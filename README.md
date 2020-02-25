# Jereloh - tech dilettante
This website is a by product of a person who cultivates an area of interest without real commitment or knowledge.

## Credits

This template was adapted from [Beautiful Jekyll](https://github.com/daattali/beautiful-jekyll). 

It is managed using:

- Github.pages
- Jekyll
- Netlify

## Docker

Local development using Docker

1. Make sure you have [Docker](https://www.docker.com/) installed.

2. Clone your repository locally.

    ```bash
    git clone https://github.com/<your_username>/<your_username>.github.io.git
    ```

3. Run the following shell commands to build the docker image and start the container for the first time:

    ```bash
    cd <repository_folder>
    docker build -t beautiful-jekyll "$PWD"
    docker run -d -p 4000:4000 --name beautiful-jekyll -v "$PWD":/srv/jekyll beautiful-jekyll
    ```


You only need to run the above once to set up Docker. You can now view your website at http://localhost:4000/. You can start the container again in the future with:

```bash
docker start beautiful-jekyll
```

And you can stop the server with:

```bash
docker stop beautiful-jekyll
```

Whenever you make any changes to `_config.yml`, you must stop and re-start the server for the new config settings to take effect.
