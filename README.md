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
docker run -v my_volume:/usr/local/apache2/htdocs -p 8081:80 httpd
```
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/00da8cd6-18cc-473b-9dc3-b59a065b1068)

### Step 9: "httpd" default page is accessible on http://localhost:8081

![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/6ea72a37-08e8-42b1-b843-5cf584d94d42)

### Step 10: Created a new file named "about.html"
### Step 11: Copy the "about.html" file from host machine to the "my_volume"
```
docker cp about.html inspiring_lichterman:/usr/local/apache2/htdocs
```
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/a064ed6e-9d16-4815-a962-c5df913df130)


### Step 12: Verify that the "about.html" file is accessible on your host machine at http://localhost:8081/about.html.
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/9d92c2d5-b352-453e-b484-b467ca88048d)

### Step 13: Stop and remove the container
```
docker stop inspiring_lichterman
```
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/9365ba8c-2320-41e6-bf61-66fbe1502a6c)

```
docker rm inspiring_lichterman
```
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/7bec6fa8-9bf4-4d07-bf08-09f36ec4ee47)

### Step 14: Verify that the "index.html" and "about.html" files are still available in the "my_volume" volume. 

![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/b06e0350-5752-461e-a48c-0a850effee19)

### Step 15: Cleanup: Remove the "my_volume" volume. 
```
docker volume rm my_volume
```
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/1ec936ca-83aa-4ed5-a66c-df4f465ddb06)






