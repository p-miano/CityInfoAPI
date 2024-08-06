# CityInfo API

## Overview
CityInfo API is a web API designed to provide detailed information about various cities and their points of interest. This project was developed as part of the ASP.NET Core Web API Fundamentals course by Plural Sight to learn and implement various technologies in the ASP.NET Core ecosystem.

## Features

### Technical Specifications

- Developed using Microsoft Visual Studio 2022.
- Frameworks and Technologies Used:
  - **ASP.NET Core**
  - **Entity Framework Core**
  - **ASP.NET Core MVC**
  - **AutoMapper**
  - **Serilog**
  - **Swagger/OpenAPI**
  - **SQLite**
  - **Azure Key Vault**
- Utilizes Entity Framework Core for database management.
- Implements a layered architecture with separation of concerns.
- Provides comprehensive logging and configuration management.

### User Roles and Operations

1. **API Consumers**
   - Retrieve information about cities.
   - Retrieve information about points of interest within a city.
   - Add, update, and delete points of interest.

### Business Rules

- Cities must have a name and description.
- Points of interest must include a name, description, and a link to a city.
- Cities and points of interest data should be managed consistently.

### Functionalities

- **City Management:** Retrieve, add, and update city information.
- **Point of Interest Management:** Retrieve, add, update, and delete points of interest within a city.
- **Logging:** Comprehensive logging using Serilog for debugging and monitoring.
- **Configuration Management:** Centralized configuration using `appsettings.json` and Azure Key Vault.
- **Email Services:** Local and cloud-based email notification services.
- **Swagger:** API documentation and testing using Swagger/OpenAPI.
- **Authentication:** JWT Bearer token authentication.

## Setup and Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/p-miano/CityInfoAPI.git
    cd CityInfoAPI/CityInfo.API
    ```
2. Restore NuGet packages:
    ```sh
    dotnet restore
    ```
3. Update the database connection string in the `appsettings.json` file.
4. Create the database using Entity Framework Core migrations:
    - Open the Package Manager Console in Visual Studio.
    - Run the command `Update-Database` to create the database schema and populate initial data.

## Database Setup

1. Ensure that you have SQLite installed and running.
2. Update the `appsettings.json` file with your SQLite connection string.
3. Open the Package Manager Console in Visual Studio.
4. Run the command `Update-Database` to create the database and tables, and to insert initial data.

## Usage

1. Launch the application:
    ```sh
    dotnet run
    ```
2. The API will be available at `https://cityinfoapi-2024.azurewebsites.net`.
3. Navigate to `https://cityinfoapi-2024.azurewebsites.net/swagger` to explore and test the API endpoints using the Swagger UI.

## Deployment to Azure Web Services

The CityInfo API has been deployed to Azure Web Services, making it accessible over the internet.

### Steps to Deploy

1. **Create an Azure Web App**:
    - Go to the Azure portal and create a new Web App.
    - Configure the Web App with the desired settings (e.g., runtime stack, region).

2. **Configure Deployment**:
    - Set up continuous deployment from your GitHub repository to the Azure Web App.
    - Go to the Deployment Center in the Azure portal, and link your GitHub repository.

3. **Set Environment Variables**:
    - In the Azure portal, go to the Configuration section of your Web App.
    - Add the necessary environment variables, such as connection strings and authentication settings.

4. **Deploy the Application**:
    - Once configured, Azure will automatically deploy your application from the GitHub repository.

### Key Vault Integration

- The application uses Azure Key Vault for managing secrets like database connection strings and JWT authentication keys.
- Ensure that the Azure Key Vault is properly configured and the secrets are added to it.
- Update the application to fetch secrets from the Azure Key Vault using the `DefaultAzureCredential`.

### Access the Deployed API

- The API is available at: `https://cityinfoapi-2024.azurewebsites.net`
- You can access the Swagger UI for testing the endpoints at: `https://cityinfoapi-2024.azurewebsites.net/swagger`

### Notes

- Ensure that the JWT Bearer token is included in the `Authorization` header for secured endpoints.
- The API is configured to use a SQLite database hosted within the Azure Web App.

## What I Learned

- **ASP.NET Core:** Gained practical experience in building a web API using ASP.NET Core.
- **Entity Framework Core:** Learned how to use Entity Framework Core for database management.
- **AutoMapper:** Implemented object-object mapping to simplify data transformation.
- **Serilog:** Configured comprehensive logging for the application.
- **Swagger/OpenAPI:** Enabled API documentation and testing with Swagger.
- **Layered Architecture:** Understood the importance of a layered architecture in maintaining separation of concerns.
- **Azure Deployment:** Gained experience in deploying applications to Azure Web Services.
- **Azure Key Vault:** Implemented secure management of application secrets using Azure Key Vault.

## Conclusion

This project was a valuable learning experience in using various ASP.NET Core technologies for API development. It provided practical skills in building a robust and scalable web API with comprehensive logging, configuration management, and API documentation. These skills are essential for future projects as a .NET developer.
