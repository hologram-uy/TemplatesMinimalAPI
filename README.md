# Minimal API with .NET Core and C#
Template for a minimal API creation with an example of a /product endpoint por references purposes

## Overview
This project demonstrates a **Minimal API** built with **.NET Core** and **C#**, implementing basic CRUD operations for a `Product` entity. Minimal APIs offer a lightweight way to create HTTP APIs with minimal dependencies and configurations.

## Features
- **Route Groups**: Organizes API endpoints for better structure.
- **Endpoint Filters**: Adds custom validation and processing logic.
- **CRUD Operations**: Supports Create, Read, Update, and Delete actions.
- **JSON Serialization**: Handles request/response formatting.

## Technologies Used
- **.NET Core**
- **C#**
- **ASP.NET Minimal API**

## Installation

1. **Clone the repository:**
   ```sh
   git clone https://github.com/hologram-uy/TemplatesMinimalAPI.git
   cd minimal-api-dotnet
   ```

2. **Build and Run the Project:**
   ```sh
   dotnet build
   dotnet run
   ```

3. **Test API Endpoints:**
   - You can test using **Postman**, **curl**, or **Swagger UI**.

## API Endpoints

### `GET /products`
Returns the list of all products.

### `GET /products/{id}`
Fetches a specific product by ID.

### `POST /products`
Adds a new product.
- **Request Body:**
  ```json
  {
    "id": 6,
    "productName": "Keyboard"
  }
  ```

### `PUT /products/{id}`
Updates an existing product.
- **Request Body:**
  ```json
  {
    "productName": "Mechanical Keyboard"
  }
  ```

### `DELETE /products/{id}`
Removes a product from the collection.

## Route Groups
The API uses **route groups** to organize related endpoints under `/products`. This improves maintainability and readability.
```csharp
var mapGroup = app.MapGroup("/products").ProductsAPI();
```

## Endpoint Filters
Custom filters are implemented to validate product data before processing the request.
```csharp
.AddEndpointFilter<CustomEndpointFilter>()
```

## License
This project is open-source and available under the [MIT License](LICENSE).

## Author
https://github.com/hologram-uy/