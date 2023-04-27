# REST API using NodeJS & Mongo DB

## API documentation

_http://[site]:[port]/api/endpoints_

## Endpoints: 
### /user
* *user/signup* [POST]
   - Sign up as a new user
   - Required json body params - ‘email’, ‘password’
* *user/login* [POST]
   - Login with existing creds
   - Required json body params - ‘email’, ‘password’

### /store
* */store* [GET] 
  - Get list of books available in store
* */store/title* [GET] 
  - Get book filtered by title
* */store* [POST]
  - Add new books to the store
  - Required json body params - ‘title’, ‘desc’, ‘price’

### /orders
* */orders* [GET]
  - Get list of orders placed by the logged in user
* */orders/orderID* [GET]
  - Get a particular order
* */orders/title* [POST]
  - Place order of a book based on the title provided
  - Required json body params - ‘id’ and title’

### NOTE: 
* POST requires authorization bearer token to be provided in headers.

* Create a file db.js in /backend/config/
    ```console
    // db.js
    module.exports = '{URL}'; 
    ```

### Example 1: Adding a new book /api/store

