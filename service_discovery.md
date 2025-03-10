## Learn Service discovery
Step 1: Create 2 ec2 instance with public IPaddress (amazon linux)
```
sudo yum install nginx -y  # Amazon Linux
sudo systemctl enable --now nginx
echo "Hello from Service 1" | sudo tee /usr/share/nginx/html/index.html
```
for server 2

```
sudo yum install nginx -y  # Amazon Linux
sudo systemctl enable --now nginx
echo "Hello from Service 2" | sudo tee /usr/share/nginx/html/index.html
```
Step 2: Verify if the webpage works.
![Screenshot 2025-03-10 at 10 04 03 PM](https://github.com/user-attachments/assets/c958f079-9526-4fed-94a0-c0b9f00004db)

![Screenshot 2025-03-10 at 10 16 11 PM](https://github.com/user-attachments/assets/41c65418-4c60-4178-be0a-8d18b0e11624)

