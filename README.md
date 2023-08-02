# About

This is a container setup for laravel + inertia, the framework is not relevant, but this example is using ReactJS configuration. 

# Commands:

1. docker compose up -d
2. docker-compose exec app bash
3. npm run dev

# Common Errors:

A. Additional config to Vite.js:

watch: {
        usePolling: true,
        origin: 'http://localhost'
    },
    server: {
        hmr: {
            host: 'localhost'
    }
}

B. Additional config "--host localhost" to "dev" in package.json

"scripts": {
        "dev": "vite --host localhost",
        "build": "tsc && vite build"
},

4. Done!

# Extra: running with Laravel Sail

<ol>
    <li>alias sail='[ -f sail ] && sh sail || sh vendor/bin/sail'</li>
    <li>sail up -d</li>
    <li>Set vite and package.json extra config (see common errors topic)</li>
    <li>Run "sail artisan route:clear" to avoid vite error from the next command 
        <ul>
            <li>Src: https://laracasts.com/discuss/channels/laravel/laravel-9-with-sail-vite-inertia-and-vue-hmr-not-working</li>
        </ul>
    </li>
    <li>sail npm run dev </li>
    <li>Done!</li>
</ol>




