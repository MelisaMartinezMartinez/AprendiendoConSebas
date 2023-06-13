# Getting Familiar with Docker

We here host a bunch of excercises that will help us to get familiar with Docker. Each of the excercises will have its own folder and we describe them below.

## Baby steps

The purpose is to get familiar with building simple images and running containers. Task description:

1. Create a Dockerfile that starts from python 3.7
2. Create an image from such docker file
3. Execute a container in interactive mode from the resulting image
4. Enter into the container and start python, then run `print("Sebas is the best")`

### Solution

```bash
cd babySteps
docker build . -t babysteps:latest
docker run -it babysteps:latest
python # inside the container
print("Sebas is the best") # in the python interpreter started from the previous command
```


## Toddler steps

Task description:

1. Create a file called "app.py" that contains the code line: `print("Meli is the second best")`.
2. Create a Dockerfile that starts with Python 3.9 and copy the file "app.py" to the root directory.
3. Create an image from such docker file.
4. Create a container from the resulting image.
5. Enter into the container and start python, then run `print("Sebas is the best")`.

## Teenager steps

1. Create a file called "app.py" that contains the code line: `print("Meli is the second best")`.
2. Create a Dockerfile that starts with Python 3.10, copy the file "app.py" to the root directory and run the command python app.py
3. Create an image from such docker file.
4. Create a container from the resulting image.
5. Run the container without getting into the container. 

## Junior Engineer level 0
1. Create a container with Python 3.10
2. Inside the container, install [FastAPI](https://fastapi.tiangolo.com)
3. Inside the container create a file called `main.py` with the contents of [the first FastAPI example found in the documentation](https://fastapi.tiangolo.com/#example).
4. Inside the container, execute the example using `uvicorn` as shown in the FastAPI guide. 
5. Inside the container, make requests using [`curl`](https://curl.se/docs/manpage.html) to validate that everything works. 

## Junior Engineer level 0.1
1. Create a file named `main.py` with the contents of [the first FastAPI example found in the documentation](https://fastapi.tiangolo.com/#example).
2. Create a container with Python 3.10, FastAPI installed and the file `main.py`.
3. Inside the container, execute the example using `uvicorn` as shown in the FastAPI guide. 
4. Inside the container, make requests using [`curl`](https://curl.se/docs/manpage.html) to validate that everything works. 

## Junior Engineer level 0.2
1. Do steps 1 and 2 from previous task
2. Run the container mapping inside the container to ports on the host, so that we can use the application from the host machine.
3. Outside the container, make requests using [`curl`](https://curl.se/docs/manpage.html) to validate that everything works. 
4. Open the docs page of the FastAPI app and validate that you can make requests as explained in FastAPI docs (see https://fastapi.tiangolo.com/#interactive-api-docs).
5. Answer the question: why is step 2 required to perform 3 and 4?
