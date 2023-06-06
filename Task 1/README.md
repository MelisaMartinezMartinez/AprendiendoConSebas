# Getting Familiar with Docker

We here host a bunch of excercises that will help us to get familiar with Docker. Each of the excercises will have its own folder and we describe them below.

## Baby steps

The purpose is to get familiar with building simple images and running containers. Task description:

1. Create a Dockerfile that starts from python 3.7
2. Create an image from such docker file
3. Create a container from the resulting image
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

1. Create a file called "app.py" that contains the code line: "print("Meli is the second best")".
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
