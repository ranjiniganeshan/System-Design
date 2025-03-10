## Learn Service discovery
* Step 1: Create 2 ec2 instance with public IPaddress (amazon linux)
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
* Step 2: Verify if the webpage works.
![Screenshot 2025-03-10 at 10 24 07 PM](https://github.com/user-attachments/assets/b79e8e19-81fd-4717-ab0d-6b13a5b07966)

![Screenshot 2025-03-10 at 10 25 48 PM](https://github.com/user-attachments/assets/60480387-6499-42cd-aa68-5225c4653d3e)

Step 3: Create a A record in go daddy

![Screenshot 2025-03-10 at 10 27 11 PM](https://github.com/user-attachments/assets/47744895-fb7c-4673-986a-7801e2472c90)

Step 4: Create a SRV record in go daddy

![Screenshot 2025-03-10 at 10 28 05 PM](https://github.com/user-attachments/assets/25a72d85-6191-4a2b-a36b-65c9fe08fa94)



