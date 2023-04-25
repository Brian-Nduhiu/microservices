# Microservice list

## User Management (UserService)

- Register a new user
- Authenticate a user (login)
- Update user profile
- Retrieve user profile
- Delete a user

## Product Management (ProductService)

- Add a new product
- Retrieve a product by ID
- Retrieve a list of products (with pagination and filters)
- Update a product
- Delete a product

## Category Management (CategoryService)

- Add a new category
- Retrieve a category by ID
- Retrieve a list of categories
- Update a category
- Delete a category

## Order Management (OrderService)

- Create a new order
- Retrieve an order by ID
- Retrieve a list of orders (with pagination and filters)
- Update an order status
- Delete an order

## Cart Management (CartService)

- Add an item to the cart
- Retrieve the cart contents
- Update the quantity of an item in the cart
- Remove an item from the cart
- Clear the cart

## Inventory Management (InventoryService)

- Update product stock
- Retrieve stock level of a product
- Monitor stock levels and trigger alerts

## Payment Processing (PaymentService)

- Process a payment
- Refund a payment
- Retrieve payment history

# Data Models & API Endpoints

## User Management (UserService)

Data Models:

User: id, firstName, lastName, email, password, role, createdAt, updatedAt
API Endpoints:

POST /register
POST /login
GET /profile/:userId
PUT /profile/:userId
DELETE /profile/:userId

## Product Management (ProductService)

Data Models:

Product: id, name, description, price, imageUrl, categoryId, createdAt, updatedAt
API Endpoints:

POST /products
GET /products/:productId
GET /products
PUT /products/:productId
DELETE /products/:productId

## Category Management (CategoryService)

Data Models:

Category: id, name, createdAt, updatedAt
API Endpoints:

POST /categories
GET /categories/:categoryId
GET /categories
PUT /categories/:categoryId
DELETE /categories/:categoryId

## Order Management (OrderService)

Data Models:

Order: id, userId, status, createdAt, updatedAt
OrderItem: id, orderId, productId, quantity, price, createdAt, updatedAt
API Endpoints:

POST /orders
GET /orders/:orderId
GET /orders
PUT /orders/:orderId
DELETE /orders/:orderId

## Cart Management (CartService)

Data Models:

CartItem: id, userId, productId, quantity, createdAt, updatedAt
API Endpoints:

POST /cart
GET /cart/:userId
PUT /cart/:cartItemId
DELETE /cart/:cartItemId
DELETE /cart/:userId

## Inventory Management (InventoryService)

Data Models:

ProductStock: id, productId, quantity, createdAt, updatedAt
API Endpoints:

PUT /inventory/:productId
GET /inventory/:productId

## Payment Processing (PaymentService)

Data Models:

Payment: id, userId, orderId, status, amount, createdAt, updatedAt
API Endpoints:

POST /payments
POST /payments/refund
GET /payments/:userId
