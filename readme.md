https://medium.com/@xroms123/docker-%E5%BB%BA%E7%AB%8B-nginx-%E5%9F%BA%E7%A4%8E%E5%88%86%E4%BA%AB-68c0771457fb

# Create the nginx server by docker build
1. build the images with name "nginxcontainer"
```
docker build -t nginxcontainer .
```

2. run the images
```
docker run --name nginx -p 8080:80 -d nginxcontainer
```

3. Check localhost:8080 


# Create the nginx server directly
1. Pull the nginx images
```
docker pull nginx
```

2. If you run the command, the nginx server will start at port 8080
```
docker run --name nginxContainer1 -p 8080:80 -d nginx
```
(Check localhost:8080, you will see the nginx default index) 

3. Start the nginx server with the mount of index.html
```
docker run --name nginxContainer1 -p 8080:80 -v index.html:/usr/share/nginx/html -d nginx
```

(Check localhost:8080, you will see the index.html) 
