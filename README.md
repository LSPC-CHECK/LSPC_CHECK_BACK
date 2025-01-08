# LSPC_CHECK_BACK
Repository of the LSPC-CHECK project developed by the JJEAR Technologies development team, its main function is to record the entry and exit of computers to and from a facility.

## Technologies Used

- **Node.js** - JavaScript runtime.
- **Express** - Web framework for Node.js.
- **PostgreSQL** - SQL database.
- **Sequelize** - ORM object modeling.
- **Bcryptjs** - Password encryption and comparison.
- **jsonwebtoken** - User authentication with JWT.
- **Babel** - JavaScript transpiler for modern JavaScript features.
- **(Others)...**

## Features

- **User Authentication** - Registration, login, and JWT token generation.
- **User Management** - CRUD operations (Create, Read, Update, Delete) for user data.
- **Computer Management** - CRUD operations (Create, Read, Update, Delete) for Computer data.
- **Profile Management** - CRUD operations (Create, Read, Update, Delete) for Profile data.
- **PQRS Management** - CRUD operations (Create, Read, Update, Delete) for PQRS data.
- **EntSal Management** - CRUD operations (Create, Read, Update) for EntSal data.
- **Security** - Password hashing, token verification for protected routes.

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/LSPC-CHECK/LSPC_CHECK_BACK.git
   cd LSPC_CHECK_BACK
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file with the following environment variables:
   ```bash
    DATABASE_HOST = your-url-host
    DATABASE_USER = your-user-database
    DATABASE_PASSWORD = your-password-database
    DATABASE_NAME = your-name-database
    DATABASE_DIALECT = your-dialect
    AUTH_TOKEN_KEY = your-jwt-secret-key
    PORT = your-port
    BUCKET_USER_PROFILE_IMAGES_NAME = your-bucket-name
   ```

4. Run the server in development mode:
   ```bash
   npm run dev
   ```

5. The server will be running on `http://localhost:4000`.

## Endpoints

### User Endpoints

- `POST /api/user/` - Create a new user.(protected)
- `POST /api/user/login/` - User login (returns a JWT).
- `GET /api/user/` - List all users (protected).
- `GET /api/user/count/` - Counts all records. (protected).
- `GET /api/user/:id` - Get user by ID (protected).
- `GET /api/user/view/image/:imageName` - Get image by computer image name (protected).
- `PUT /api/user/:id` - Update user information (protected).
- `DELETE /api/user/:id` - Delete user by ID (protected).

### Computer Endpoints

- `POST /api/computer/` - Create a new computer (protected).
- `GET /api/computer/` - List all computers.(protected).
- `GET /api/computer/:id` - Get computer by ID (protected).
- `GET /api/computer/count/` - Counts all records (protected).
- `GET /api/computer/pcUser/:idUser` - Get computer linked to each UserID (protected).
- `PUT /api/computer/:id` - Update computer information (protected).
- `DELETE /api/computer/:id` - Delete computer by ID (protected).

### PQRS Endpoints

- `POST /api/pqrs/` - Create a new pqrs (protected).
- `GET /api/pqrs/` - List all pqrs (protected).
- `GET /api/pqrs/:id` - Get pqrs by ID (protected).
- `GET /api/pqrs/` - Counts all records (protected).
- `GET /api/pqrs/userPqrs/:idUser` - Get pqrs linked to each UserID (protected).
- `PUT /api/pqrs/:id` - Update pqrs information (protected).
- `DELETE /api/pqrs/:id` - Delete pqrs by ID (protected).

### EntSal Endpoints

- `POST /api/entSal/` - Create a new entSal (protected).
- `GET /api/entSal/` - List all entSal (protected).
- `GET /api/entSal/:id` - Get entSal by ID (protected).
- `GET /api/entSal/` - Counts all records (protected).
- `PUT /api/entSal/:id` - Update entSal information (protected).
- `DELETE /api/entSal/:id` - Delete entSal by ID (protected).

### Profile Endpoints

- `POST /api/profile/` - Create a new profile (protected).
- `GET /api/profile/` - List all profile (protected).
- `GET /api/profile/:id` - Get profile by ID (protected).
- `GET /api/profile/` - Counts all records (protected).
- `PUT /api/profile/:id` - Update profile information (protected).
- `DELETE /api/profile/:id` - Delete profile by ID (protected).

### Recommended and/or used profiles
- **Administrator**
- **Directivas**
- **Management Administrative Assistant**
- **User**

### Additional information:
Some functions are under development, such as the uploading of images in the configuration / profile update section, in addition to the functions that depend on this same, so there is no concern if there are failures related to these components.

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.