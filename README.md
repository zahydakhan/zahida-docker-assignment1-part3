# zahida-docker-assignment1-part3
### Step 1: Created a volume "my_volume"

![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/90ec4c09-571c-4569-87f0-dcc8b0523c51)

### Step 2: Create a new Docker container using the "nginx" image and mount the "my_volume" volume to the container's "/usr/share/nginx/html" directory.
```
docker run -v my_volume:/usr/share/nginx/html -p 8080:80 nginx
```
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/de5769f1-73cf-4066-99ae-cbc240f59cd3)

### Step 3: Verify that the "nginx" default page is accessible on your host machine at http://localhost:8080
![image](https://github.com/zahydakhan/zahida-docker-assignment1-part3/assets/45081511/af3bd371-5bed-4763-bd8f-0f18508e2b90)

