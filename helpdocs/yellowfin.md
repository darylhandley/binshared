# nvm stuff if you need to set node versions
nvm use 
nvm install 24 
nvm use 24 

# bring up all services locally 
docker compose up 
docker compose up --build 

# dbs in docker and others in dev mode
docker compose up dynamodb-local dynamodb-init postgres

# backend on 8090 
cd yellowfin-backend
set -a; source ../.env; set +a
mvn spring-boot:run -Dspring-boot.run.profiles=local -Djooq.codegen.skip=true

# frontend on 3000
cd yellowfin-frontend
npm install && npm run dev 

# lamnbdas on 3001
cd lambdas 
yarn install 
yarn local-dev

# run smoke tests - edit .env to set the lambdas to run against
cd smoke-tests 
npm test 
npm run test:npm
