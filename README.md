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

## Get a product

**GET /products/:productId**

Returns a single product from the inventory.

#### Parameters

| Name          | Type    | In    | Required | Description                                  |
|---------------|---------|-------|----------|----------------------------------------------|
| productId     | integer | path  | Yes      | Specifies the product's id you wish to retrieve. |
| product-label | boolean | query | No       | Returns the product label in PDF format.     |

#### Status codes

| Status code   | Description                                    |
|---------------|------------------------------------------------|
| 200 OK        | Indicates a successful response.               |
| 404 Not Found | Indicates that there is no product with the specified id. |

## Cart

### Get a cart

**GET /carts/:cartId**

Returns a cart.

#### Parameters

| Name   | Type   | In   | Required | Description                    |
|--------|--------|------|----------|--------------------------------|
| cartId | string | path | Yes      | Specifies the id of the cart you wish to retrieve. |

#### Status codes

| Status code   | Description                                    |
|---------------|------------------------------------------------|
| 200 OK        | Indicates a successful response.               |
| 404 Not Found | Indicates that there is no cart with the specified id. |

### Get cart items

**GET /carts/:cartId/items**

Returns the items in a cart.

#### Parameters

| Name   | Type   | In   | Required | Description                    |
|--------|--------|------|----------|--------------------------------|
| cartId | string | path | Yes      | Specifies the id of the cart for which you wish to retrieve the items. |

#### Status codes

| Status code   | Description                                    |
|---------------|------------------------------------------------|
| 200 OK        | Indicates a successful response.               |
| 404 Not Found | Indicates that there is no cart with the specified id. |

### Create a new cart

To create a new cart, submit an empty POST request to the /carts endpoint.

**POST /carts**

Creates a new cart and returns the id in the response body.

#### Parameters

No parameters are accepted for this request.

#### Status codes

| Status code   | Description                                    |
|---------------|------------------------------------------------|
| 201 Created   | Indicates that the cart has been created successfully. |

#### Example response body

```json
{
  "created": true,
  "cartId": "bx0-ycNjqIm5IvufuuZ09"
}
