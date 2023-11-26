# docker-test
Creating a repo with docker testing to run a python Hello World program

Ensure that docker engine is installed and running in the background

Clone the repository in your home directory using 'git clone'

Navigate to the `dockertest` directory

Run the command - `docker build -t python_test:1.0 .`

Run `docker images` to see whether the python_test image with version 1.0 has been built or not

After checking that the image has been built succesfully, run `docker run -d -p 5000:5000 python_test:1.0`

Navigate to localhost:5000 to ensure that the host port has been succesfully mapped to the container port and Hello World appears on your screen

You can pull this image from my dockerhub using `docker pull adimish545/python_test`

# flask_test

This folder contains a slightly more advanced flask webpage. Pull this image from my dockerhub using `docker pull adimish545/sample_flask`. Or directly download and run on your system and build the image using the provided Dockerfile.
