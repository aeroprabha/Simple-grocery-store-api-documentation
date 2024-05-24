# Simple Grocery Store API

This API allows you to place a grocery order which will be ready for pick-up in the store.  
The API is available at [https://simple-grocery-store-api.glitch.me](https://simple-grocery-store-api.glitch.me)  
Alternative URL: [http://simple-grocery-store-api.online/](http://simple-grocery-store-api.online/) (HTTP only!)

## Endpoints

- **Status**
- **Products**
  - Get all products
  - Get a product
- **Cart**
  - Get a cart
  - Get cart items
  - Create a new cart
  - Add an item to cart
  - Modify an item in the cart
  - Replace an item in the cart
  - Delete an item in the cart
- **Orders**
  - Get all orders
  - Get a single order
  - Create a new order
  - Update an order
  - Delete an order
- **API Authentication**
  - Register a new API client

## Status

### GET /status

Returns the status of the API. Example response:

```json
{
  "status": "UP"
}
