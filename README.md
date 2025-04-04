# Scaleable Chat Application

A scalable chat application built with a modern monorepo architecture using Turborepo, Next.js, Prisma, Kafka, Redis, and Socket.IO.

## Features

- **Real-time Chat**: Powered by Socket.IO for instant communication.
- **Scalable Architecture**: Kafka and Redis for message queuing and pub/sub.
- **Database Management**: Prisma ORM with PostgreSQL.
- **Monorepo**: Managed with Turborepo for efficient development and builds.
- **Frontend**: Built with Next.js for both `web` and `docs` apps.

## Monorepo Structure

This project is organized as a monorepo with the following structure:

### Apps

- **`web`**: The main chat application built with Next.js.
- **`server`**: The backend server handling WebSocket connections, Redis, Kafka, and Prisma.
- **`docs`**: Documentation site built with Next.js.

### Packages

- **`ui`**: Shared React components used across apps.
- **`eslint-config`**: Shared ESLint configurations.
- **`typescript-config`**: Shared TypeScript configurations.

## Prerequisites

- Node.js (v18 or higher)
- PostgreSQL database
- Redis server
- Kafka broker
- Yarn (v1.22 or higher)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/scaleable-chat.git
   cd scaleable-chat
   ```

2. Install dependencies:
   ```bash
   yarn install
   ```

3. Configure environment variables:
   - Create `.env` files in the `server` and `web` apps with the required variables (e.g., `DATABASE_URL`, `REDIS_URL`, `KAFKA_BROKER_URL`).

4. Generate Prisma client:
   ```bash
   cd apps/server
   npx prisma generate
   ```

5. Apply database migrations:
   ```bash
   npx prisma migrate dev
   ```

## Running the Application

### Development

1. Start the backend server:
   ```bash
   cd apps/server
   yarn dev
   ```

2. Start the frontend app:
   ```bash
   cd apps/web
   yarn dev
   ```

3. Start the documentation site:
   ```bash
   cd apps/docs
   yarn dev
   ```

### Production

1. Build all apps:
   ```bash
   yarn build
   ```

2. Start the server:
   ```bash
   cd apps/server
   yarn start
   ```

3. Serve the frontend and documentation apps using a production-ready server.

## Technologies Used

- **Frontend**: Next.js, React
- **Backend**: Node.js, Socket.IO, Prisma, Kafka, Redis
- **Database**: PostgreSQL
- **Monorepo Management**: Turborepo

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.
