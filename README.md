# About

This is a container setup for Laravel and Inertia.

# Production

1. docker compose up -d
2. docker-compose exec app bash
3. composer install
4. npm install
5. Laravel deployment commands - https://laravel.com/docs/10.x/deployment
6. npm run build
7. Go to localhost:80
8. Done!

# Development

NodeJS can run on local machine for development.

1. docker compose up -d
2. docker-compose exec app bash
3. composer install 
4. Laravel deployment commands - https://laravel.com/docs/10.x/deployment
5. exit 
6. npm run dev
7. Go to localhost:80
8. Done!

# Errors and solutions:

<p>ERR_CONNECTION_REFUSED</p>
<p>Solution: delete public/hot and rebuild the application</p>






