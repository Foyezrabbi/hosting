```code 
sudo apt update
```

```code 
sudo adduser rabbi
```

```code 
sudo adduser rabbi sudo
```

```code 
sudo apt install nginx
```

```code 
sudo nano /etc/nginx/sites-enabled/flask_app
```

```code 
server {
    listen 80;
    server_name foyezrabbi.com https//www.foyezrabbi.com;

    location / {
        proxy_pass http://127.0.0.1:8000;
        proxy_set_header Host $host;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }
}
```

```code 
sudo unlink /etc/nginx/sites-enabled/default
```

```code 
sudo nginx -s reload
```

```code 
sudo apt install python3
```

```code 
sudo apt install python3-pip
```

```code 
cd /home/rabbi
```

```code 
sudo apt install gunicorn3
```

```code 
sudo gunicorn3 --workers=3 run:app
```

