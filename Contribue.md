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
- Start postgres
  - docker run -e POSTGRES_PASSWORD=myseceretpassowrd -p 5432:5432 run postgres
- Build the image - `docker build --network=host -t user-project . `
- Start the image - `docker run -p 3000:3000 user-project`

## Docker Compose Installation Steps

- Install docker, docker-compose
- Run `docker-compose up`
