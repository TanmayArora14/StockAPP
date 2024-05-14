                                                                            Deploying MERN Stack Application on Render
Prerequisites:-

    a)Node.js and npm installed locally
    b)MongoDB Atlas account (or any other MongoDB hosting provider)
    c)Render account

1. Set Up MongoDB Database

    a)Sign up or log in to your MongoDB Atlas account.
    b)Create a new cluster and configure it according to your needs.
    c)Obtain your MongoDB connection string.

2. Clone the Repository

git clone https://github.com/yourusername/your-mern-app.git
cd your-mern-app

3. Configure MongoDB Connection

    a)Open server.js file in the root directory of your project.
    b)Locate the MongoDB connection configuration.
    c)Replace the placeholder with your MongoDB connection string.

mongoose.connect('your_mongodb_connection_string', { useNewUrlParser: true, useUnifiedTopology: true });

4. Install Dependencies
npm install

5. Build the React App
npm run build

6. Create Render YAML Configuration

    Create a render.yaml file in the root directory of your project.
    Add the following configuration:
services:
    name: your-mern-app
    type: web
    buildCommand: npm install && npm run build
    startCommand: npm start

7. Deploy to Render

    a)Sign up or log in to your Render account.
    b)Create a new web service and choose the GitHub repository where your MERN app is located.
    c)Configure your MongoDB connection string in Render's dashboard.
    d)Click "Deploy" to deploy your MERN app.

8. Access Your Deployed Application

Once the deployment is complete, your MERN stack application will be accessible via the provided URL.
