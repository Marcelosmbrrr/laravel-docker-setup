# About

This is a container setup for laravel + inertia for development and production. 

# Commands for production:

1. docker compose up -d
2. docker-compose exec app bash
3. composer install + npm install
4. Laravel deployment commands - https://laravel.com/docs/10.x/deployment
5. npm run build
6. Done!

# Error and solution:

<p>ERR_CONNECTION_REFUSED</p>
<p>Solution: delete public/hot and rebuild the application</p>

# Commands for development:

1. docker compose up -d
2. docker-compose exec app bash
3. composer install + npm install
4. exit and npm run dev
5. Done!

# Error and solution:

"Unable to locate file in Vite manifest"

Additional config to Vite.js:

    watch: {
            usePolling: true,
            origin: 'http://localhost'
        },
        server: {
            hmr: {
                host: 'localhost'
        }
    }

Additional config "--host localhost" to "dev" in package.json: 

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




