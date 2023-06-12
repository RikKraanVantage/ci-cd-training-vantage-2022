# Vantage CI/CD training
The idea of this hands-on is to generate a CI/CD pipeline based on this dummy repository.

## Setup

- Use your own Github account to fork this repository.
- Create a virtual environment
- You can train new models or change something in the code as you like
- **Now** create your CI/CD Pipeline
  - It should have linting
  - Testing
  - Deploying a new model

For the deployment of the Docker that has the predict endpoint I used Heroku. 
1. Create an account on https://id.heroku.com/login.
2. Secondly, create a new app with the naming `employee-predict-vantage-{YOUR_NAME}`.
3. Then, install Heroku CLI using `brew tap heroku/brew && brew install heroku` for MAC.
4. Create an API key using `heroku authorizations:create` which can somehow be used in your CI/CD pipeline

Make sure you push the container to your own app name. Change this in `app/app.py`.
Finally, you can check on Heroku logs if the container is deployed successfully and check if you can predict by running:
``streamlit run /app/app.py``

