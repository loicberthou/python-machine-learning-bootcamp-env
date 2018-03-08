# MachineLearning 
## Start Jupyter
In the terminal:
```
cd ~/MachineLearning
docker-compose up -d
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
docker-compose down
```
