# NGINX configs

```
git clone https://github.com/kelseyhightower/nginx-summit-portland.git
sudo cp nginx-summit-portland/nginx/*.conf /etc/nginx/conf.d/
```

```
sudo docker run -d --net=host \
  -v /etc/nginx/nginx.conf:/etc/nginx/nginx.conf \
  -v /etc/nginx/conf.d:/etc/nginx/conf.d \
  nginx
```
