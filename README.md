# zahida-docker-assignment1-part3
### Step 1: Created a volume "my_volume"
```
docker volume create my_volume
```

![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/bd410e80-e11e-4d89-830e-6bf1184e082d)

### Step 2: Create a new Docker container using the "nginx" image and mount the "my_volume" volume to the container's "/usr/share/nginx/html" directory.
```
docker run -v my_volume:/usr/share/nginx/html -p 8080:80 nginx
```
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/eb09edd9-3fe7-428e-8737-34f794d002ac)

### Step 3: Verify that the "nginx" default page is accessible on your host machine at http://localhost:8080
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/b9e869ca-a22e-472b-be50-efb05ec5a13b)

### Step 4: Created a new file named "index.html" and added some text to it.

### Step 5: Copied the "index.html" file from host machine to the "my_volume" volume using the "docker cp" command.
```
docker cp index.html relaxed_feistel:/usr/share/nginx/html
```
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/9333392a-65d9-4543-a3b3-87be9be60e12)

### Step 6: Verify that the "index.html" file is accessible on your host machine at http://localhost:8080. (2 marks)
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/40ab9b8a-32ca-45ca-9d2b-76f029a24f11)

### Step 7: Stop and remove the container
```
docker stop relaxed_feistel
```
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/64a0d884-83f6-4640-a10e-5b95f27d2619)

```
docker rm relaxed_feistel
```
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/b5a40a98-cfab-49c7-aa6f-941d90f87537)

### Step 8: Created a new Docker container using the "httpd" image and mount the "my_volume" volume to it at "/usr/local/apache2/htdocs"
```
docker run -v my_volume:/usr/share/nginx/html -p 8080:80 nginx
```
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/00da8cd6-18cc-473b-9dc3-b59a065b1068)

### Step 9: "httpd" default page is accessible on http://localhost:8081

![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/6ea72a37-08e8-42b1-b843-5cf584d94d42)

### Step 10: Created a new file named "about.html"
### Step 11: Created a new file named "about.html"
marks)


![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/4c9ec063-0992-4bf3-8069-47e956d01465)






