# timarttest
This is a take home test (nodejs,express,graphql,mysql)

Here are the instructions for running the Node.js application that exposes GraphQL endpoints for creating a new user, retrieving user information by ID, creating a new order for a user, and retrieving a user's orders, using Express.js and GraphQL for routing and Sequelize for MySQL database interactions, and implementing proper input validation and error handling in the API endpoints:


##Instructions:
Clone the repository to your local machine.
Install Node.js and npm on your system.
Open the terminal and navigate to the project directory.
Run the command npm install to install the required dependencies.
Create a MySQL database and update the database configuration in the models/index.js file.
Run the command npm start to start the server.
Open a web browser and navigate to http://localhost:3000/graphql to access the GraphQL playground.
Use the GraphQL queries and mutations to create a new user, retrieve user information by ID, create a new order for a user, and retrieve a user's orders.
GraphQL Queries and Mutations:
To create a new user:


mutation {
  createUser(input: { name: "John Doe", email: "johndoe@example.com" }) {
    id
    name
    email
  }
}

To retrieve user information by ID:
query {
  user(id: 1) {
    id
    name
    email
    orders {
      id
      date
      amount
    }
  }
}

To create a new order for a user:
mutation {
  createOrder(input: { date: "2023-10-20", amount: 100.0, userId: 1 }) {
    id
    date
    amount
    user {
      id
      name
      email
    }
  }
}


To retrieve a user's orders:
query {
  orders(userId: 1) {
    id
    date
    amount
    user {
      id
      name
      email
    }
  }
}


Note: Replace the user ID and order details with your own values.







