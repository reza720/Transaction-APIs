## Steps to Create These APIs
- Step 1: Define Use Cases
- Step 2: Define Business Rules
- Step 3: Design Domain Models
- Step 4: Design APIs (Routes)
- Step 5: Implement Services & Controllers

## Install These Tools
  - Express
  - ORM: Sequelize, MySQL2
  - Logging: Winston
  - Security Libs: Express-validator, JWT & bcrypt/Argon2, Helmet, express-rate-limit, CORS, hpp 
  - Testing: Jest, Supertest, Postman or cUR, K6, OWASP ZAP, SonarQube
  - Dotenv
  - API Doc: Swagger
  - Mirgration: sequelize-cli 
  - Nginx 
  - Redis
  - Webhooks
  - Caching: Redis  
  - Reverse Proxy: Nginx    
  - IDE: VS Code
  - Docker

## Setup Layers & Add Logs / Security:
  - Config Winston & Sequelize
  - write Dotenv & constants
  - Write Models
  - Write Utils if needed any time for any part
  - Write Simple service layer: + signup & login with JWT & bcrypt/Argon2 
  - Use Logger: Business success: in service, Failer: in globalErrorHandler, Server Events: in app and server 
  - Write Controller/Handler layer
  - Write Middleware: globalErroHandler with failer logs, Security(validations, Authentication, Authorization)
  - Write Router: middleware functions, middleware tools(specific rate limiter, Route-Specific CORS(prod only))
  - Write app: Mount routers, middlewares(Body parser, globalErrorHandler, 404 of route, Helmet, rate limiter, Cors, hpp)
  - Write server

  
  ## Apply Testing:
  - Unit Testing (jest): Write One for every service,middleware, & utils files that includes functions that has logic 
  - API Automated Testing (Jest + Supertest): Write One for every Router file that includes all Routes 
  - Performance / Load Testing: K6: Write one stress and one load for every Router that inlcudes all the routes in it
  - API Manual Testing (Postman)
  - Dependencies Testing: Use npm audit if Needed
  - Static Application Security Testing (SAST): Use SonarQube: After API is created
  - Dynamic Application Security Testing (DAST):Use OWASP ZAP After API is created
  - Debugg: VS Code Debugger / console.log: Any Error Found

## Add More Things:
  - API Doc: Swagger
  - External Services:
  - Use Webhooks
  - Cashing: Redis
  - reverse Proxy: NginX
  - Migration: sequelize-cli
  - Setup CI/CD Piplines: GitHub Actions
  - Containerize: Docker