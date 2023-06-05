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

...

## Teenager steps

...

