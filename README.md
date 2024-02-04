# Gestion-inventaire-utilsateur-et-Produits
Inventory Management API
This is a simple HTTP API for managing inventory and user information. The API provides basic CRUD (Create, Read, Update, Delete) operations for both inventory items and management users.

Inventory Controller
The InventoryController is responsible for handling requests related to inventory management.

Endpoints
GET /api/{version}/inventory

Retrieve a list of all inventory items.

GET /api/{version}/inventory/{id}

Retrieve details of a specific inventory item by providing its ID.

POST /api/{version}/inventory

Add a new inventory item by providing the necessary details in the request body.

PUT /api/{version}/inventory/{id}

Update an existing inventory item by providing its ID and the updated details in the request body.

DELETE /api/{version}/inventory/{id}

Delete a specific inventory item by providing its ID.

Management User Controller
The ManagementUserController is responsible for handling requests related to management users.

Endpoints
GET /api/{version}/users

Retrieve a list of all management users.

GET /api/{version}/users/{id}

Retrieve details of a specific management user by providing their ID.

POST /api/{version}/users

Add a new management user by providing the necessary details in the request body.

PUT /api/{version}/users/{id}

Update an existing management user by providing their ID and the updated details in the request body.

DELETE /api/{version}/users/{id}

Delete a specific management user by providing their ID.

Usage
Make HTTP requests to the specified endpoints using the appropriate HTTP methods (GET, POST, PUT, DELETE) and provide the required parameters in the request URL or body, as needed.

API Versioning
The API supports versioning, and the version is specified in the request URL. If no version is provided, the default version is assumed to be "v1."

Example
Retrieve all inventory items
Request:

http
Copy code
GET /api/v1/inventory
Response:

json
Copy code
[
  {
    "product_id": 1,
    "name": "Product A",
    "quantity": 50,
    "price": 19.99
  },
  {
    "product_id": 2,
    "name": "Product B",
    "quantity": 30,
    "price": 29.99
  }
  // ... other inventory items
]
Retrieve details of a specific inventory item
Request:

http
Copy code
GET /api/v1/inventory/1
Response:

json
Copy code
{
  "product_id": 1,
  "name": "Product A",
  "quantity": 50,
  "price": 19.99
}
Add a new inventory item
Request:

http
Copy code
POST /api/v1/inventory
Content-Type: application/json

{
  "name": "New Product",
  "quantity": 10,
  "price": 39.99
}
Response:

json
Copy code
{
  "message": "Inventory item added successfully."
}

Error Handling
If an error occurs, the API will respond with an appropriate HTTP status code and an error message in the response body.
