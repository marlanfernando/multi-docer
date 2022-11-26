# Docker with muti container deployment

In this section its focused to deploy multiple containers using docker-compose. the end goal of this example is to create run and deploy these artifacts in to AWS beanstalk.

Further in this example we use pushing the created containers to dockerhub, so the beanstalk does not need to rebuild the containers again

# Used technologies
    Docker
    Travis
    AWS beanstalk
    JS
    postgrss
    redis

# Travis flow for deployment
    1. Specify docker as dependancy
    2. Build test version of react project
    3. Run tests
    4. Build prod version of all projects
    5. Push all to dockerhub
    6. Tell EBS to update

# Travis multi container setup ( extended )
    1. push code to github
    2. Travis pulls repo
    3. Travis builds the test image, test code
    4. Travis builds prod image
    5. Travis pushes built prod images to docker-hub
    6. Travis pushes project to EBS
    7. EBS pulls images from docker hub and deploy

