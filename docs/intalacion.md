# Installation and Execution

## 1. Requirements

Before running CineWeb, install the following tools:

- Node.js
- pnpm
- MySQL Server
- Git

## 2. Database Setup

CineWeb uses MySQL for data persistence. The backend uses MikroORM 6 to access the database.

### 2.1. Create the Database

1. Start the MySQL server.
2. Execute the `init.sql` script provided in the backend repository.
3. Make sure the database is named `che_netflix`, as required by the backend configuration.

### 2.2. Configure Environment Variables

1. In the backend repository, copy `.env.example` to a new file named `.env`.
2. Configure the MySQL connection using the following variables:
   - `MYSQL_HOST`: MySQL server host.
   - `MYSQL_USER`: MySQL username.
   - `MYSQL_PASSWORD`: MySQL password.
   - `MYSQL_PORT`: MySQL server port.
   - `MYSQL_DATABASE`: database name (`che_netflix`).
   - `MYSQL_DEBUG`: enables or disables SQL query logging.
3. Configure the API port using `PORT` (default: `3000`).
4. Set `CORS_ORIGIN` to the frontend origin. The default development origin is `http://localhost:5173`.
5. Keep `CONTENT_DIR` set to the directory used to store uploaded videos and thumbnails.
6. Configure `MAX_VIDEO_SIZE_MB` and `MAX_IMAGE_SIZE_MB` to set upload size limits.

Use your own local database credentials in `.env`. Do not commit this file or publish passwords in the repository.

## 3. Backend Setup

1. Clone the backend repository:

   ```bash
   git clone https://github.com/EduardoMarino73/TP-BackEnd.git
   ```

2. Enter the project directory:

   ```bash
   cd TP-BackEnd
   ```

3. Install dependencies:

   ```bash
   pnpm install
   ```

4. Configure the environment variables as described in Section 2.2.

5. Start the development server:

   ```bash
   pnpm run start:dev
   ```

The backend is configured to listen on port `3000`.

## 4. Frontend Setup

1. Clone the frontend repository:

   ```bash
   git clone https://github.com/liamlucca/cineweb-frontend.git
   ```

2. Enter the project directory:

   ```bash
   cd cineweb-frontend
   ```

3. Install dependencies:

   ```bash
   pnpm install
   ```

4. Start the development server:

   ```bash
   pnpm run dev
   ```

Open the local URL displayed in the terminal to access the application. By default, Vite uses `http://localhost:5173`.

## 5. Running the Application

To run CineWeb locally:

1. Make sure the MySQL server is running and the database has been created.
2. Start the backend using `pnpm run start:dev`.
3. In a separate terminal, start the frontend using `pnpm run dev`.
4. Open the local URL displayed by the frontend development server.

Keep both development servers running while using the application.
