# About

This is a container setup for laravel + inertia, the framework is not relevant, but this example is using ReactJS configuration. 

# Commands for production:

a. docker compose up -d
b. docker-compose exec app bash
c. composer install + npm install
d. npm run build
e. Done!

# Errors:

ERR_CONNECTION_REFUSED
Solution: delete public/hot and rebuild the application

# Commands for development:

a. docker compose up -d
b. docker-compose exec app bash
c. composer install + npm install
d. exit and npm run dev
e. Done!

# Error:

"Unable to locate file in Vite manifest"

Solution: Additional config to Vite.js:

    watch: {
            usePolling: true,
            origin: 'http://localhost'
        },
        server: {
            hmr: {
                host: 'localhost'
        }
    }

Solution: Additional config "--host localhost" to "dev" in package.json: 

    "dev": "vite --host localhost",

# Extra: about Laravel Sail

<ol>
    <li>alias sail='[ -f sail ] && sh sail || sh vendor/bin/sail'</li>
    <li>sail up -d</li>
    <li>Set vite and package.json extra config (see common errors topic)</li>
    <li>Run "sail artisan route:clear" to avoid vite error when run "sail npm run dev"
        <ul>
            <li>https://laracasts.com/discuss/channels/laravel/laravel-9-with-sail-vite-inertia-and-vue-hmr-not-working</li>
        </ul>
    </li>
    <li>sail npm run dev </li>
    <li>Done!</li>
</ol>




