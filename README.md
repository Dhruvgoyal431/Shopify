# Shopify

Instead of going to the local malls for a shopping spree, more and more people are using the variety of online resources to discover the right products for them. From giants like Amazon to small Etsy stores, online shopping is the future of consumerism!
This project is a web based shopping system.This project is an attempt to provide the advantages of online shopping to customers of a real shop. It helps buying the products in the shop anywhere. Thus the customer will get the service of online shopping and home delivery from his favorite shop. This system can be implemented to any shop in the locality or to multinational branded shops having retail outlet chains. If shops are providing an online portal where their customers can enjoy
easy shopping from anywhere, the shops won’t be losing any more customers to the trending online shops such as flipcart or ebay. Since this is a website it is easily accessible and always available.
### App Description:
    1. user can view all products
    2. user can view single product
    3. user can search products and view products by category and price range
    4. user can add to cart checkout products using credit card info
    5. user can register & sign in
    6. admin can create, edit, update & delete products
    7. admin can create categories
    8. admin can view ordered products

## Demo
### Home page
![image](https://user-images.githubusercontent.com/97663545/204956116-a61dbfac-dba9-4fb5-905c-01c3a662c48e.png)
### Signin page
![image](https://user-images.githubusercontent.com/97663545/204901126-33a0e4cb-72ad-4ca6-9772-4d117d362f3e.png)
### Signup page
![image](https://user-images.githubusercontent.com/97663545/204901152-6665d796-d65f-4b16-9336-e5d523684a81.png)
### Shop page
![image](https://user-images.githubusercontent.com/97663545/204900938-cecf57ba-8dc9-4c6f-8e11-377fbeeeaec8.png)
### Single product view page
![image](https://user-images.githubusercontent.com/97663545/204955858-82911bba-44c6-40e7-9dac-515f82f81c60.png)
### Shop page(using filters)
![image](https://user-images.githubusercontent.com/97663545/204901272-cf50f3f4-a374-4c11-b4b9-1380de1a5574.png)
### Dashboard(user login)
![image](https://user-images.githubusercontent.com/97663545/204901335-281eefde-13ce-4081-8fd6-c6d3069ba7ad.png)
### Cart & checkout page
![image](https://user-images.githubusercontent.com/97663545/204901443-bb6b5ca3-6ed1-4f34-b288-6818f55a78ce.png)

### Technologies Used

> Frontend-> React JS

> Backend-> Node JS & Express JS

> Database-> MongoDB Atlas

## Installation & deployment(local server) process
1. #### clone the repo using this command
    ```bash
    git clone https://github.com/Dhruvgoyal431/Shopify.git
    ```
2. #### install npm packages
    1. install backend packages
    ```bash
    cd Shopify
    npm install
    ```
    2. install frontend packages
    ```bash
    cd client
    npm install
    ```
3. go to the parent folder of Shopify & create .env for mongodb connection, JWT_SECRET, BRAINTREE_MERCHANT_ID, BRAINTREE_PUBLIC_KEY and BRAINTREE_PRIVATE_KEY.

    ##### sample code for backend .env
    ```env
    MONGO_URI=YOUR_MONGO_URI
    JWT_SECRET=YOUR_JWT_SECRET
    BRAINTREE_MERCHANT_ID=YOUR_BRAINTREE_MERCHANT_ID
    BRAINTREE_PUBLIC_KEY=YOUR_BRAINTREE_PUBLIC_KEY
    BRAINTREE_PRIVATE_KEY=YOUR_BRAINTREE_PRIVATE_KEY
    ```
4.  create another .env file inside client directory for REACT_APP_API_URL.
    
    ##### sample code for frontend .env
    ```env
    REACT_APP_API_URL=YOUR_API_URL
    ```
    ##### Instruction:
    1. for mongodb atlas database creation follow this tutorial->https://www.youtube.com/watch?v=KKyag6t98g8
    2. you can use any random string as JWTSECRET
    3. for localhost REACT_APP_API_URL is http://localhost:5000/api
       but for heroku (server deployment) it will be different
    4. #### note: add .env on .gitignore
    5. for server deployment use secrets directly

5. <b>deploy this project</b> on your local server by using this command
    ```bash
    cd Shopify
    npm run server
    ```
    <b>In another terminal/power shell</b>
    ```bash
    cd Shopify\client
    npm start
    ```
    #### note: both backend & frontend server will start with the above commands.

6. #### Database Structure: (Table: columns)
    1. categories: _id, name, createdAt, updatedAt;
    2. orders:  _id, status, products (Array), transaction_id, amount, address, user (Object), createdAt, updatedAt
    3. products: _id, photo (Object), sold, name, description, price, category, shipping, quantity, createdAt, updatedAt
    4. users: _id, role, history (Array), name, email, salt, hashed_password, createdAt, updatedAt

## Authors
    Omkar Salvi
    Shruti Nogja
    Dhruv Goyal
