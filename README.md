# docker-nginx
nginx:
  image: nginx
  ports:
     - "80:80"
  links:
     - website
  volumes_from:
     - website

website:
  labels:
    - "Sitio web"
  image: busybox
  volumes:
    - ./public/:/usr/share/nginx/html/
