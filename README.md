# MachineLearning 
## Start Jupyter
In the terminal:
```
cd ~/MachineLearning
docker-compose up -d
```
The '-d' option means detached mode. It will start the container in the background.

Check that the container is running by typing:
```
docker ps -a
```

Open your browser and type the address:
```
http://localhost:8888/
```

## Stop Jupyter
```
# Stop but persist the notebooks folder
docker-compose down


# Stop and rebuild the notebooks folder on next start
docker-compose down -v
```

## Execute a command on the container (like a conda command)
After having started in detached mode, type in the terminal:
```
cd ~/MachineLearning
docker-compose exec jupyter3 /bin/bash
```
This will start a bash session on the container 'jupyter3' that is already running.
You should get a different prompt that indicates that you're on the container. It looks like this:
```
root@jupyter3:/# 
```
Now you can run your command. Let's install NumPy:
```
conda install numpy
```
After the install is complete, just exit the container, type:
```
exit
```
