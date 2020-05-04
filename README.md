example deployment based on testdriven.io blog

Dockerizing Django with Postgres, Gunicorn, and Nginx
Want to learn how to build this?

Check out the post.
Want to use this project?
Development

Uses the default Django development server.

    Rename .env.dev-sample to .env.dev.

    Update the environment variables in the docker-compose.yml and .env.dev files.

    Build the images and run the containers:

    $ docker-compose up -d --build

    Test it out at http://localhost:8000. The "app" folder is mounted into the container and your code changes apply automatically.

Production

Uses gunicorn + nginx.

    Rename .env.prod-sample to .env.prod and .env.prod.db-sample to .env.prod.db. Update the environment variables.

    Build the images and run the containers:

    $ docker-compose -f docker-compose.prod.yml up -d --build

    Test it out at http://localhost:1337. No mounted folders. To apply changes, the image must be re-built.
    
    
CI/CD integration   pipeline1



