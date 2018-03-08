# Images for Jupyter Notebooks

## Build & Publish the image
In a Terminal:
```
cd ~/MachineLearning/images/jupyter3
docker build -t loicberthou/jupyter3:5.1.0 .
docker login
docker push loicberthou/jupyter3:5.1.0
docker push loicberthou/jupyter3
```

## Run the image
In a terminal:
```
# In detached mode
docker run -d --rm -p 8888:8888 --name notebook-test loicberthou/jupyter3
# Stop the container when in detached mode
docker stop notebook-test

# In interactive mode
docker run -i -t --rm -p 8888:8888 --name notebook-test loicberthou/jupyter3
```

Options explained:
* -d: run the container in the background.
* --rm: delete the container instance after it stops.
* -p 8888:8888: maps the port 8888 of the container to port 8888 of the host.
* --name notebook-test: give a name to the container instance.
