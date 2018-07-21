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

**8. HTTP status code common to /{id}: GET, PUT/PATCH and DELETE is 404: Not Found**

**7. HTTP status codes specific to GET is 200: Success/Ok and specific to POST is 201: Created**

## Use Case 1: Comments

## Use Case 2: Comments

## Use Case 3: Comments
