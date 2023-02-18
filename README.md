# Jay-s_RESTful_Restaurant
A Restaurant database where you can add, edit, delete and star your favourite restaurants using an online database API.

## Server-Side API Calls to External APIs
In this tutorial, you will learn how to connect an external API to a Node.js back-end.

### Project Setup
To get started with this tutorial, make sure you download the starting and solution code. When you complete the steps in this tutorial, compare your code with the code in the solution-code folder and see how you did!

The starting-code folder contains the following sub-folders:

frontend
backend
Run the following command in both sub-folders separately to install the dependencies:
npm install

To run the application, you will need to have two separate terminal windows or tabs open: one for the frontend folder and the other for the backend folder. You will want to start the application in the backend folder, then the frontend folder. You can start the application with the following command:
npm run start

When first starting the backend server, you will see an error be thrown. This error is because the back-end is not connected to supabase yet. After you complete the steps in this tutorial, the errors will be resolved.

You will get a notification in the terminal window when starting the server in the frontend folder, stating that the port 3000 is in use and asking if you would like to use another port like below:
Would you like to run the app on another port instead? › (Y/n)
Type y in the terminal prompt to use a different port.

You are ready to get started with the tutorial steps! Note that the start command runs nodemon for the backend server and react-scripts for the frontend server. Any code changes you make in these folders will trigger the application to re-render automatically.

### Tutorial Steps
In the following steps, we will be creating PostgreSQL tables in supabase and modifying backend/provider/supabase.js to connect to your supabase database. The variables that we create in supbase.js will be exported to use supabase providers, allowing us to authenticate with the external API and make calls to supabase.

Before we start coding, you will want to familiarize yourself with the code of the following files in the starting-code folder:

backend/routes/restaurants.js and backend/routes/starredRestaurants.js
These files contain the supabase provider initialization, as well as the back-end routes for interacting with the external API.
frontend/src
The files in this folder contain the front-end code of the application, as well as the calls to the backend routes, which will make the calls to the external API.

### Creating a Supabase Database
First, navigate to supabase and create an account by selecting the “Start your project” button.

You will be asked to log in with your GitHub account. Follow the steps to allow supabase access to your GitHub account.

Next, let’s create a new project in supabase. To create a project, you will also need to create an organization. Click on the “New project” button, then click on “New organization”.

You will be prompted to first, name your organization, then to enter the name for your project and database password. Select the region of your choice, then click on the “Create new project” button.

Supabase will take a couple of minutes to generate your project. After your project is created, navigate to the "Settings" tab and scroll down to "API" and make note of the "API URL" and "API Key" as we will need these later.

### Setting up the client-side app

1. Clone this repository to your local machine: 
https://github.com/777Jaylee777/Jay-s_RESTful_Restaurant.git

2. Navigate to the cloned directory:
cd example-app

3. Install the dependencies:
npm install

4. Create a new file called .env at the root of the project:
touch .env

5. Open the .env file in your code editor and add the following environment variables:
SUPABASE_URL=your-api-url
SUPABASE_ANON_KEY=your-api-key

Replace your-api-url and your-api-key with the values you obtained from the Supabase project earlier.

6. Start the app:
This will open the app in your default browser at http://localhost:3000.

That's it! You should now have a working example app that uses Supabase as the backend. From here, you can modify the app to suit your needs and experiment with the various features offered by Supabase.
