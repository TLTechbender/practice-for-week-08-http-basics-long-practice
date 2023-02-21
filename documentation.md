============================================
============================================
## EXAMPLE DOCUMENTATION
### Ask for the Home Page
#### Step 1
Predicted Request components:
- Method: GET
- URL: http://layout.pug {I kinda thought this would be it, I didn't factor localhost into my reasoning }
Correct URL: http://localhost:5000/
I really dont' understand what this project wants me to do
- Headers: none
- Body: none

Predicted Response components:
- Status Code: 200
- Headers:
  - Content-Type: text/html
- Body: HTML page with navigation links to other pages

#### Step 2
In your browser open the chrome dev tools, navigate to [http://localhost:5000] and make a GET request for the Home Page (type "/" into the URL after 5000 and hit "enter").
Explore the "network" tab and find where you can compare your predicted request/response components to the actual components.

#### Step 3
If your prediction was wrong, try to understand why it was incorrect and then update your documentation to the correct request/response components.

Congratulations! You have performed a GET request to / showing the home page of our e-commerce
website. Move on to the next request/response documentation.

* Note
    - Headers contain many keys, but for this exercise focus on **Content-Type** and **Location**.
 
=============================================
=============================================

### Ask for a page that doesn't exist

Request components:
- Method:GET
- URL:http://localhost:5000/gbebodye
- Headers:
Content-Type:text/html
- Body:none

Response components:
- Status code:404
- Headers:Content-Type:text/html
- Body:
A error notification page

### Ask for the products list page

Request components:
- Method:GET
- URL:http://localhost:5000/products
- Headers:
Content-Type:text/html
- Body:

Response components:
- Status code: 200
- Headers:Content-Type:text/html
Correction: charset=utf-8
- Body: I dunno:
Server responds with an html page?!
A html page with a link to navigate to a particular product.

### Ask for the product detail page

Here's an example product on the server:

| detail      | value                                                      |
| ----------- | ---------------------------------------------------------- |
| productId   | 1                                                          |
| name        | "Facial Cleansing Brush"                                   |
| description | "Reaches deep pores to cleanse oil, dirt, and blackheads." |
| price       | 23.99                                                      |
| categories  | "beauty", "electronics"                                    |

Request components:
- Method:GET
- URL: http://localhost:5000/products/:productId=1/
correction:http://localhost:5000/proudcts/1
- Headers: 
Context-Type:text/html
charset=utf-
- Body:none 

Response components:
- Status code:200 
- Headers:Context-Type:text/html
- Body: A html page containing the particular product with links to other html pages

### Ask for the create new product page

Request components:
- Method:GET
- URL:http://localhost:5000/products/new
- Headers: 
Context-Type:text/html
- Body: none

Response components:
- Status code: 200
- Headers: Context-Type:text/html
- Body: 
A html page is returned by the server that contains a html form and links to navigate to other html pages.

### Submit a new product

Remember, for a traditional HTML web server, whenever a successful `POST`
request is sent to the server, the server should respond with a redirection to
a page.

After successful submission, user should be looking at the product detail page.

Here are the categories on the server:

| tag         | name           |
| ----------- | -------------- |
| grocery     | Grocery        |
| electronics | Electronics    |
| beauty      | Beauty         |
| toys-games  | Toys and Games |
| health      | Health         |
| furniture   | Furniture      |
| clothing    | Clothing       |

* Note: In Chome dev tools, if the "body" of a request exists, it will appear 
in the network tab as "payload".

Request components:
- Method:POST
- URL: http://localhost:5000/products/tag/name
correction: my url was a  wrong url.....
http://localhost:5000/products
- Headers: 
Context-Type:text/html
- Body: 
I get redirected?

Response components:
- Status code: 302
- Headers:Context-Type:text/html
- Body: Shows a successful addition of product.

### Ask for the edit product page

Request components:
- Method: Get
- URL: http://localhost:5000/products/:productId/edit
- Headers: 
Context-Type:text/html
- Body: none

Response components:
- Status code:200
- Headers: Context-Type:text/html
- Body:A html form showing me how to go about editing the product

### Submit an edit for an existing product

After successful submission, user should be looking at the product detail page.

Request components:
- Method:POST
- URL:http://localhost:5000/products/:productId/
- Headers: Context-Type:text/html
- Body: I get redirected?

Response components:
- Status code: 302
- Headers:Context-Type:text/html
- Body: A html page showiing me that my edit was successful

### Submit a delete for an existing product

After successful submission, user should be looking at the products list page.

Request components:
- Method: POST
- URL:http://localhost:5000/products/:productId/delete
- Headers: 
Context-Type:text/html
- Body: I get redirected.

Response components:
- Status code: 302
- Headers:
Context-Type:text/html
- Body: A html page showing me a successful delete.

### Submit a new review for a product

After successful submission, user should be looking at the product detail page.

Here's an example review on the server:

| detail     | value                  |
| ---------- | ---------------------- |
| reviewId   | 1                      |
| comment    | "I love this product!" |
| starRating | 5                      |
| productId  | 1                      |

Request components:
- Method: POST
- URL: http://localhost:5000/comments
correction: http://localhost:5000/products/:productId/comments
- Headers:
Context-Type:text/html
Context-Type:text/html
- Body: I get redirected

Response components:
- Status code: 302
- Headers: Context-Type:text/html
- Body: Comment gets posted

### Ask for the edit review page for a product

Request components:
- Method: GET
- URL: http://localhost:5000/products/:productId/reviews/edit
correcttion:http://localhost:5000/reviews/reviews/productId/edit
- Headers: Context-Type:text/html
- Body: none

Response components:
- Status code: 200
- Headers:Context-Type:text/html
- Body: A html page showing me how to go about editing

### Submit an edit for an existing review

After successful submission, user should be looking at the product detail page.

Request components:
- Method: POST
- URL: correction:http://localhost:5000/products/product:Id
- Headers:correction:Context-Type:text/html
- Body: I get redirected

Response components:
- Status code: 302
- Headers: Context-Type:text/html
- Body:I see that the edit works

### Submit a delete for an existing review

After successful submission, user should be looking at the product detail page.

Request components:
- Method:POST
- URL: http:localhost:5000/reviews/:productId/delete
- Headers: Context-Type:text/html
- Body: I get redirected

Response components:
- Status code: 302
- Headers: Context-Type:text/html
- Body: Stuff's deleted

### Ask for all the products in a particular category by tag of the category

Request components:
- Method: GET
- URL: http://localhost:5000/categories/tag/products
- Headers: Context-Type:text/html
- Body: none

Response components:
- Status code: 200
- Headers:Context-Type:text/html
- Body: An html page displaying the products appears

### Ask for the best-selling product

Look for clues in the HTML pages from the prior responses for what the route should be.

Request components:
- Method: GET
- URL: http://localhost:5000/categories/products/best-selling
- Headers:Context-Type:text/html 
- Body: none

Response components:
- Status code: 200
- Headers:Context-Type:text/html
- Body: I literally see the best selling product