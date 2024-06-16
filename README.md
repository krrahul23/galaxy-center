# Galaxy Center

An API demonstration project with Deno, Oak, Docker and Typescript

# Documentation:

## Deno commands:

- To run (localhost)\
  `deno run --allow-net --allow-read --allow-env src/mod.ts`

- To test\
  `deno test --allow-read`

## Docker commands:

- To build\
  `docker build -t <NAME_OF_THE_CONTAINER> .`

- To run (localhost)\
  `docker run -it -p 8000:8000 <CONTAINER_LOCATION_ON_DOCKER_HUB>`

- To run (deployment)\
  `docker run -it -p 8000:8000 --restart=always <CONTAINER_LOCATION_ON_DOCKER_HUB>`

## Deployment (on heroku)

- Step 1: Login\
  `heroku login`  
  `heroku container:login`

- Step 2: Create heroku app\
  `heroku create`\
  NOTE: This step will return the name of the app which was created, please copy it, it will be needed for the next step (For example: abc_xyz_1234.herokuapp.com, abc_xyz_1234 is the app name)

- Step 3: Push container to heroku\
  `heroku container:push web -a <APP_NAME>`

- Step 4: Release container to heroku\
  `heroku container:release web -a <APP_NAME>`

- Step 5: Launch!\
  `heroku open -a <APP_NAME>`

Congratulations! Your app is now deployed!

NOTE: In order to update the container, repeat steps 1, 3 and 4 (step 1 if not logged in)
