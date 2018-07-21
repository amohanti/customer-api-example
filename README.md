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


## Use Case 1: Comments

## Use Case 2: Comments

## Use Case 3: Comments
