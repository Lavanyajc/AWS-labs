Just use data while creating instance
---

### `user-data.sh`

```bash
#!/bin/bash
# Use this for your user data (script from top to bottom)
# Install Apache Web Server
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html

