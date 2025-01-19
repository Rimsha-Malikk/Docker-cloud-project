# Docker-cloud-project
# Restaurant Management System (Microservices-based)

## Overview
This project is a microservices-based Restaurant Management System developed using Docker Compose. It consists of four services:

1. **Frontend Service**: Provides an interactive user interface for managing the restaurant system.
2. **Menu Service**: Handles the restaurant's menu items.
3. **Order Service**: Manages customer orders.
4. **User Service**: Manages user accounts and details.

The services are interconnected to create a seamless system for restaurant management. All services are containerized using Docker.

---

## Project Structure
```
restaurant-system/
|
├── frontend/
│   ├── app.py
│   ├── templates/
│   │   └── index.html
│   └── Dockerfile
|
├── menu-service/
│   ├── app.py
│   ├── requirements.txt
│   └── Dockerfile
|
├── order-service/
│   ├── app.py
│   ├── requirements.txt
│   └── Dockerfile
|
├── user-service/
│   ├── app.py
│   ├── requirements.txt
│   └── Dockerfile
|
└── docker-compose.yml
```

---

## Features
- **Frontend Service**: Displays the restaurant's menu, manages orders, and allows user interaction.
- **Menu Service**: CRUD operations for menu items (add, update, delete, and fetch menu items).
- **Order Service**: Processes orders and integrates with the menu and user services.
- **User Service**: Handles user information and integrates with the order service.

---

## Requirements
- Docker
- Docker Compose
- Python (for local testing, if needed)

---

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd restaurant-system
   ```

2. Build the Docker images:
   ```bash
   docker-compose build
   ```

3. Start the services:
   ```bash
   docker-compose up
   ```

4. Access the application:
   - Frontend Service: [http://localhost:5000](http://localhost:5000)
   - Menu Service: [http://localhost:5004/menu](http://localhost:5004/menu)
   - Order Service: [http://localhost:5003/orders](http://localhost:5003/orders)
   - User Service: [http://localhost:5002/users](http://localhost:5002/users)

5. Stop the services:
   ```bash
   docker-compose down
   ```

---

## API Endpoints

### Menu Service
- **GET** `/menu`: Fetch all menu items.
- **POST** `/menu`: Add a new menu item.

### Order Service
- **GET** `/orders`: Fetch all orders.
- **POST** `/orders`: Place a new order.

### User Service
- **GET** `/users`: Fetch all users.
- **POST** `/users`: Add a new user.

---

## Modifications for Dynamic Data
To allow users to input data dynamically, forms were added in the frontend for:
- Adding menu items (menu name and price).
- Placing orders (select menu items and quantities).

---

## Technologies Used
- **Backend**: Python (Flask)
- **Frontend**: HTML, CSS, Bootstrap
- **Containerization**: Docker, Docker Compose

---

## Challenges Faced
- Debugging indentation errors in Python scripts.
- Resolving container networking issues.
- Integrating services to work seamlessly.

---

## Future Enhancements
- Improve the UI with a modern framework (e.g., React or Vue.js).
- Add authentication and authorization for users.
- Include database integration for persistent data storage.

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---



