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
- **Configuration Management:** Centralized configuration using `appsettings.json`.
- **Email Services:** Local and cloud-based email notification services.
- **Swagger:** API documentation and testing using Swagger/OpenAPI.

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
2. The API will be available at `https://localhost:5001` or `http://localhost:5000`.
3. Navigate to `https://localhost:5001/swagger` or `http://localhost:5000/swagger` to explore and test the API endpoints using the Swagger UI.

## What I Learned

- **ASP.NET Core:** Gained practical experience in building a web API using ASP.NET Core.
- **Entity Framework Core:** Learned how to use Entity Framework Core for database management.
- **AutoMapper:** Implemented object-object mapping to simplify data transformation.
- **Serilog:** Configured comprehensive logging for the application.
- **Swagger/OpenAPI:** Enabled API documentation and testing with Swagger.
- **Layered Architecture:** Understood the importance of a layered architecture in maintaining separation of concerns.

## Conclusion

This project was a valuable learning experience in using various ASP.NET Core technologies for API development. It provided practical skills in building a robust and scalable web API with comprehensive logging, configuration management, and API documentation. These skills are essential for future projects as a .NET developer.
