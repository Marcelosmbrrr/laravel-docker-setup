# About

This is a container setup for laravel + inertia, the framework is not relevant, but this example is using ReactJS configuration. 

# Commands:

1. docker compose up -d
2. docker-compose exec app bash
3. npm run dev

# Common Errors:

1. Additional config to Vite.js:

watch: {
        usePolling: true,
        origin: 'http://localhost'
    },
    server: {
        hmr: {
            host: 'localhost'
    }
}

2. Additional config "--host localhost" to "dev" in package.json

"scripts": {
        "dev": "vite --host localhost",
        "build": "tsc && vite build"
},


