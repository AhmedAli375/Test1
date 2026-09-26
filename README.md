<h1 align="center">
  <a href="https://nestify.systems/"><img src="https://github.com/AhmedSalman1/E-Commerce-API/blob/main/assets/logo.png" alt="Nestify" width="150"></a>
  <br>
  Nestify
  <br>
</h1>

<p align="center">
  <a href="https://nodejs.org/">
    <img src="https://img.shields.io/badge/Node.js-v16-green.svg" alt="Node.js">
  </a>
  <a href="https://expressjs.com/">
    <img src="https://img.shields.io/badge/Express.js-v4.18.2-blue.svg" alt="Express.js">
  </a>
  <a href="https://www.mongodb.com/">
    <img src="https://img.shields.io/badge/MongoDB-v6.x-brightgreen.svg" alt="MongoDB">
  </a>
  <a href="https://aws.amazon.com/">
    <img src="https://img.shields.io/badge/AWS-S3%20%7C%20EC2-orange.svg" alt="AWS">
  </a>
  <a href="https://jestjs.io/">
    <img src="https://img.shields.io/badge/Jest-Testing-orange.svg" alt="Jest">
  </a>
  <a a href="https://stripe.com/">
    <img src="https://img.shields.io/badge/Stripe-Payment-blue.svg" alt="Stripe">
  </a>
</p>

<h4 align="center">
  An E-Commerce API built with Node.js, Express.js, MongoDB, and integrated with AWS and Stripe. Designed for robust and scalable online shopping experiences.
</h4>

 <p align="center">
 <a href="#deployed-version">Demo</a> •
  <a href="#key-features">Key Features</a> •
  <a href="#technical-highlights">Technical Highlights</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#api-routes">API Routes</a> •
  <a href="#api-usage">API Usage</a> •
  <a href="#built-with">Built With</a> •
  <a href="#my-development-practices">My Practices</a>
</p>

---

## Deployed Version

> **Note:** Live deployment is currently offline (AWS Free Tier expired).
> Feel free to test it locally or check out the [Postman Documentation](https://documenter.getpostman.com/view/30055418/2sAYBUCBuW)

- 🔗 **Live Demo (Offline):** https://nestify.systems/

---

## Key Features

- **Authentication & Authorization** 🚀
  - Sign up, login, logout, password reset, and **_Google OAuth_** integration.
  - Role-based access control (admin, user, manager) with **_JWT authentication_**.
- **User Profile** 🧑‍💼
  - Users can **_update their profile_**, including username, email, and password.
  - **_Admins_** can manage all user profiles.
- **Product Catalog & Search** 🛒
  - **_Browse_** and **_search products_** by **_categories, brands_**, and other filters.
  - Powerful **_search functionality_** to find products quickly.
  - **_Admins can manage products_** (add, update, delete).
- **Shopping Cart & Checkout** 🛍️
  - **_Add products to cart_** and **_checkout securely_** with **_Stripe payments_**.
- **Order Management** 📦
  - Users can **_track order history_** and **_shipping status_**.
  - Admins manage orders and process refunds.
- **Reviews & Ratings** 🌟
  - Users can **_leave reviews_** for purchased products; **_admins_** can delete inappropriate ones.
- **Discounts & Coupons** 💸
  - Apply **_discount codes_** at checkout; **_admins_** manage promotions.
- **Favorites** ❤️
  - Users can save **_favorite products_** for future purchases.

---

## Technical Highlights

| **Feature**                        | **Description**                                                           |
| ---------------------------------- | ------------------------------------------------------------------------- |
| **Authentication & Authorization** | Google OAuth integration via Passport.js for seamless user login.         |
| **Role-Based Access Control**      | Admin, user, and manager roles with granular permissions.                 |
| **AWS S3**                         | Efficient cloud storage for serving and managing product images.          |
| **Stripe Payment Gateway**         | Secure and reliable payment processing for customer transactions.         |
| **Validation**                     | Strong input validation using `express-validator` ensures data integrity. |
| **Unit & Integration Testing**     | Comprehensive test coverage ensures API reliability and stability.        |
| **AWS Deployment**                 | Scalable and high-performance hosting using AWS EC2.                      |

---

## API Routes

The following routes are available for interacting with the API:

- All routes are prefixed with `/api/v1/`. For example, to access the orders endpoint, use `/api/v1/orders`.

| **Resource**       | **Route**        | **Methods**              |
| ------------------ | ---------------- | ------------------------ |
| **Categories**     | `/categories`    | GET, POST, PATCH, DELETE |
| **Subcategories**  | `/subcategories` | GET, POST, PATCH, DELETE |
| **Brands**         | `/brands`        | GET, POST, PATCH, DELETE |
| **Products**       | `/products`      | GET, POST, PATCH, DELETE |
| **Users**          | `/users`         | GET, POST, PATCH, DELETE |
| **Authentication** | `/auth`          | GET, POST, PATCH         |
| **Reviews**        | `/reviews`       | GET, POST, PATCH, DELETE |
| **Favorites**      | `/favorites`     | GET, POST, DELETE        |
| **Addresses**      | `/addresses`     | GET, POST, DELETE        |
| **Coupons**        | `/coupons`       | GET, POST, PATCH, DELETE |
| **Cart**           | `/cart`          | GET, POST, PATCH, DELETE |
| **Orders**         | `/orders`        | GET, POST, PATCH         |

---

## API Usage

Before using the API, you need to set the variables in Postman depending on your environment (development or production). Simply add:

```
- {{URL}} with your hostname as value (Eg. http://127.0.0.1:3000/ or https://nestify.systems/)
- {{password}} with your user password as value.
```

For more info check API Documentation on Postman 👉🏻 [E-Commerce API Documentation](https://documenter.getpostman.com/view/30055418/2sAYBUCBuW).

---

## How To Use

You can get the E-Commerce API up and running on your local machine using the following steps:

1.  **Fork or Git-clone:**

    - You can fork the app on GitHub or git-clone it into your local machine.

    ```bash
    git https://github.com/AhmedSalman1/E-Commerce-API.git
    cd e-commerce-api
    ```

2.  **Install Dependencies and Set Environment Variables:**

    - In the root directory of the app, create a file named `.env`.

    ```bash
    $ npm install
    Set your env variables(like: .env.example)
    ```

3.  **Run Commands:**

    ```
    $ npm run start (for development)
    $ npm run start:prod (for production)
    ```

4.  **Run Tests:**

    ```
    $ npm run test
    ```

- Run specific test files:

  ```
  $ npm run test --file tests/auth.test.js
  ```

---

## Built With

- [NodeJS](https://nodejs.org/en/) - JavaScript runtime environment
- [Express](http://expressjs.com/) - The web framework used
- [Mongoose](https://mongoosejs.com/) - Object Data Modelling (ODM) library
- [MongoDB Atlas](https://www.mongodb.com/cloud/atlas/) - Cloud database service
- [AWS EC2](https://aws.amazon.com/ec2/) - Cloud computing service for hosting the application
- [AWS S3](https://aws.amazon.com/pm/serv-s3/) - Cloud storage for managing and serving images
- [Google OAuth](https://console.cloud.google.com/) - Authentication via Google account
- [Stripe](https://stripe.com/) - Online payment API for handling payments
- [Jest](https://jestjs.io/) - JavaScript testing framework for unit and integration tests
- [Mailgun](https://www.mailgun.com/) - Email delivery platform for transactional emails
- [Postman](https://www.getpostman.com/) - API testing and documentation tool

---

## My Development Practices

I adhere to these practices to ensure a maintainable and scalable codebase:

- Use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) for meaningful and consistent commit messages.
- Follow a structured [branching strategy](#branching-strategy) for organized version control.
- Maintain clean and readable code by sticking to [Clean Code Guidelines](#clean-code-guidelines).
- Ensure all contributions pass linting and tests before integration.

These principles guide my work to deliver high-quality, reliable, and scalable software.

---

## Conclusion

- Thank you for exploring this E-Commerce API built with NodeJS. This project is designed to provide a robust backend for online shopping platforms, with features like authentication, product management, and secure payment processing.

- Feel free to clone the repository, contribute, or open issues for any questions or bugs.
