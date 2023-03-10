```code
ssh root@IP_Address -p 22
```

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
cd /home/rabbi/foyezrabbi
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
    server_name foyezrabbi.com;

    location / {
        proxy_pass http://127.0.0.1:5000;
        proxy_set_header Host $host;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }
}
```

```code 
sudo unlink /etc/nginx/sites-enabled/default
```

```code 
sudo nginx -t
```
```code
sudo systemctl restart nginx
```

```code 
sudo nginx -s reload
```
```code 
sudo apt install python3
```

```code 
python3 -m venv venv
```

```code 
source venv/bin/activate
```
```code 
pip install -r requirements.txt
```
```code 
sudo apt install gunicorn3
```

```code 
sudo gunicorn3 --workers=3 run:app
```
```code
sudo gunicorn3 --bind 0.0.0.0:8000 --workers=3 run:app
```

```code
pkill gunicorn3 #to kill all gunicorn3
```

```code
sudo fuser -k 8000/tcp  #to kill the port
```
```code
sudo ufw allow 8000
```
```code
nohup /path/to/test.py &
```
```code
ps ax | grep test.py
```
```code
sudo killall {processName = python}
```

