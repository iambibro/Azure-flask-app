# Flask Application on Azure Web App

## Overview

This repository contains a simple Flask application deployed to Azure Web Apps. The application features a single endpoint that returns "Hello, Azure Web Apps!" when accessed.

## GitHub Repository

**Repository URL:** [https://github.com/iambibro/Azure-flask-app](https://github.com/iambibro/Azure-flask-app)

## Project Structure

```
/Azure-flask-app
  ├── .github/
  │   └── workflows/
  │       └── azure-webapp.yml
  ├── app.py
  ├── requirements.txt
  ├── README.md
```

## Setup Instructions

To set up and run the project locally:

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/iambibro/Azure-flask-app.git
   ```

2. **Create and Activate a Virtual Environment:**

   - On Windows:
     ```bash
     python -m venv venv
     venv\Scripts\activate
     ```

   - On Unix/macOS:
     ```bash
     python -m venv venv
     source venv/bin/activate
     ```

3. **Install Dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Application Locally:**

   ```bash
   python app.py
   ```

   Access the application at `http://127.0.0.1:5000`.

## Deployment Instructions

The application is deployed to Azure Web Apps via GitHub Actions. Follow these steps to ensure proper deployment:

1. **Create Azure Web App:**
   - Navigate to the Azure Portal and create a new Azure Web App with the following settings:
     - **Subscription:** Your Azure subscription
     - **Resource Group:** Create a new or use an existing one
     - **Name:** A unique name for the Web App
     - **Publish:** Code
     - **Runtime stack:** Python (selected the appropriate version)
     - **Region:** Choose a region close to you

2. **Set Up GitHub Actions:**
   - The GitHub Actions workflow file (`.github/workflows/azure-webapp.yml`) automates deployment.
   - Add your Azure publish profile to GitHub Secrets with the name `AZURE_WEBAPP_PUBLISH_PROFILE`.

3. **Push to GitHub:**
   - Commit and push changes to the `main` branch to trigger the deployment process.

## Confirm Deployment

Ensure the application is deployed and accessible:

1. **Verify Deployment:**
   - Visit the Azure Web App's URL: `https://flask-app-03-eycabug5g9frdadf.canadacentral-01.azurewebsites.net`
   - The application should display "Hello, Azure Web Apps!".

2. **Check GitHub Actions Logs:**
   - In your GitHub repository, go to the **"Actions"** tab to view the status of the deployment workflow.

## Live Application
The live application is available at:  `https://flask-app-03-eycabug5g9frdadf.canadacentral-01.azurewebsites.net`

## Contact

For any questions or support, please contact [your-email@example.com](mailto:your-email@example.com).

---