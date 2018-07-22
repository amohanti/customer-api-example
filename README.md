# Title: customer-api-example
*Description: Customer RESTful API example for Deloitte*

# Problem Statement

*Design/Specification for Customers REST API*

*Resource: Customers*

*Operations:* 

*1. Get a single/all customers (GET)*

*2. Create a new customer (POST)*

*3. Update a customer (PATCH/PUT)* 

*4. Delete a customer (DELETE)*

*Attributes: First Name, Last Name, Addresses*

*Relationships: Orders API, Products API*

*Use Cases:*

*1. Periodic 5 minute consumption of API and consumer maintains a copy of all customers obtained from provider*

*2. Mobile App uses API to retrieve and update customer details*

*3. Simple Extension of API to support future resources such as Products and Orders*

## General Notes/Comments

**1. Main API file is customer-api-example.raml where resource is customers**

**2. Secondary API files are order-api-example.raml where resource is orders and product-api-example where resource is products**

**3. The customer API has the ability to retrieve a single customer by ID or all customers**

**4. The customer API has the ability to create a single customer and return the ID as well as update/delete customer by ID**

**5. The customer attributes used in the API are First Name, Last Name and Addresses which is a collection of multiple addresses that a customer can have e.g. primary and secondary address**

**6. HTTP status codes common to GET, POST, PUT/PATCH and DELETE are 401: Unauthorized, 500: Internal Server Error and 504: Gateway Timeout**

**7. HTTP status code common to /{id}: GET, PUT/PATCH and DELETE is 404: Not Found**

**8. HTTP status code specific to GET is 200: Success/Ok and specific to POST is 201: Created**

**9. The customers API design can be made even simpler and better by recognizing similar patterns and eliminating code redundancy by implementing Reource Types and Traits. E.g. Responses of 401, 500 and 504 can easily be represented as traits**

## Use Case 1: Comments

**1. Consumer gets all customers from API, which has Header with etag and lastmodified timestamp**

**2. Consumer stores the customer record with the retrieved timestamp**

**3. Consumer sleeps for 5 minutes**

**4. Consumer gets all customers from API, which has Header with etag and lastmodified timestamp**

**5. Consumer validates customers against its stored values using ID and lastmodified timestamp**

## Use Case 2: Comments

**1. For the mobile App to retrive a particular customer from the API, it needs to provide an App ID, CSR/User ID and Customer ID to the API**

**2. The API uses queryParameters of App ID and User ID to return a response back to the mobile App**

**3. The mobile App uses customer ID and PATCH method to update the customer details back into the API**

**4. Patch is a more network efficient way to update as compared to Put**

## Use Case 3: Comments

**1. Orders and Products have been designed as two different APIs**

**2. Orders is included as a sub-resource under Customers**

**3. lineItems is a complex type under Orders, where one order can have multiple line items**

**4. Product is again included as a sub-resource under lineItems where each line item has one product associated**

**5. This design caters for the use case to make the Customers API easily extendable to include Orders and Products**


