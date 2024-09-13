# About

This is a container setup for any version of Laravel vanilla, Laravel with Inertia and Livewire.

# Production

1. docker compose up -d
2. docker-compose exec app bash
3. npm install
4. Laravel deployment commands - https://laravel.com/docs/10.x/deployment
5. npm run build
6. Go to localhost:8000
7. Done!

# Development

NodeJS can run on local machine for development.

1. docker compose up -d
2. docker-compose exec app bash
3. Laravel deployment commands - https://laravel.com/docs/10.x/deployment
4. exit 
5. npm run dev
6. Go to localhost:8000
7. Done!

# Errors and solutions:

<p>ERR_CONNECTION_REFUSED</p>
<p>Solution: delete public/hot and rebuild the application</p>






