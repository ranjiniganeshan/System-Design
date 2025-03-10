## Learn Service discovery
Step 1: Create 2 ec2 instance with public IPaddress (amazon linux)
```
sudo yum install nginx -y  # Amazon Linux
sudo systemctl enable --now nginx
echo "Hello from Service 1" | sudo tee /usr/share/nginx/html/index.html
```
for server 2

```
```
sudo yum install nginx -y  # Amazon Linux
sudo systemctl enable --now nginx
echo "Hello from Service 2" | sudo tee /usr/share/nginx/html/index.html
```
Step 2: Verify if the webpage works.

![Screenshot 2025-03-10 at 10 16 36 PM](https://github.com/user-attachments/assets/407bf033-15f0-4b47-ab93-994626009c43)
![Screenshot 2025-03-10 at 10 04 03 PM](https://github.com/user-attachments/assets/ae357cfd-1b69-4191-b2bd-418804c669ec)
