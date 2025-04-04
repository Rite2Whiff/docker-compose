## Manual Installation

- Install nodejs locally()
- Clone the repo
- Install dependencies(npm install)
- Start the DB locally
  - docker run -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
  - Go to neon.tech and get yourself a new DB
- Change the .env file and update your DB credentials
- npx prisma migrate dev
- npx prisma generate
- npm run build
- npm run start

## Docker Installation

- Install Docker
- Start a new network `docker network create user_project`
- Start postgres
  - docker run --network user_project --name postgres -e POSTGRES_PASSWORD=mysecretpassword -p 5432:5432 postgres
- Build the image - `docker build --network=host -t user-project . `
- Start the image - `docker run --network user_project -e DATABASE_URL=postgresql://postgres:mysecretpassword@postgres:5432/postgres -p 3000:3000 user-project`

## Docker Compose Installation Steps

- Install docker, docker-compose
- Run `docker-compose up`
