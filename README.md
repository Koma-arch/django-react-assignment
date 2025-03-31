# Project Overview

## Django Backend

### Features:
- Django project with Django Rest Framework (DRF) for RESTful APIs.
- Item model with fields: name, description, price, category, etc.
- Serializer for converting the model to JSON.
- ViewSets for CRUD operations.
- Filtering capabilities for searching, ordering, and filtering by various fields.
- Sample data generation script for testing.

### Endpoints:
#### Admin Interface:
- [Admin Panel](http://localhost:8000/admin/)
  - Login with the superuser credentials.

#### API Root:
- [API Root](http://localhost:8000/api/)
  - Displays all available endpoints.

#### Items Endpoint:
- [Items API](http://localhost:8000/api/items/)
  - `GET`: List all items (paginated).
  - `POST`: Create a new item.
  - `PUT/PATCH`: Update an item.
  - `DELETE`: Delete an item.

### Filtering Examples:
- **By category:** [Filter by Category](http://localhost:8000/api/items/?category=electronics)
- **By stock:** [Filter by Stock](http://localhost:8000/api/items/?in_stock=true)
- **By price range:** [Filter by Price Range](http://localhost:8000/api/items/?price_min=100&price_max=500)
- **Search:** [Search Items](http://localhost:8000/api/items/?search=keyword)
- **Ordering:** [Order by Price](http://localhost:8000/api/items/?ordering=price)

### Backend is Complete With:
- Django with DRF (using SQLite for simplicity).
- Model for the data table.
- Full CRUD APIs.
- Filtering and searching capabilities.
- Pagination for API responses.

---

## React Frontend

### Features:
- React application using Vite as the build tool.

### Components:
- `ItemTable`: Displays the list of items.
- `ItemFilter`: Filters items based on criteria.
- `CategoryGroups`: Displays items grouped by category.
- `ItemForm`: Used for creating and editing items.
- `ConfirmationModal`: Handles item deletion confirmation.
- `Pagination`: Enables navigating through pages.

### Pages:
- `ItemListPage`: Main page with CRUD functionality.
- `CategoryGroupsPage`: Displays items grouped by category.

### Service and Utilities:
- `api.js`: Handles communication with the backend.
- `formatters.js`: Formats currency, dates, etc.
- Routing is implemented using React Router.

### Functionality:
- Viewing items in a table.
- Filtering items by various criteria.
- Sorting items by clicking on column headers.
- Creating, editing, and deleting items.
- Viewing items grouped by category with statistics.

### Access:
- [Application](http://localhost:5173/)
- [Category Groups View](http://localhost:5173/categories)

### Backend Communication:
- The frontend communicates with the Django backend running at [http://localhost:8000/api/](http://localhost:8000/api/).
