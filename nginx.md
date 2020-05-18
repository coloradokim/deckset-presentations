footer: @kimschles

## nginx and Node.js 

### Kim Schlesinger

#### Denver Node.js Meetup - May 2020 

--- 

# Agenda 
1. Facts about nginx   
1. Demo setup 
1. nginx as a
    * Reverse Proxy 
    * Web Cache
    * Load Balancer 
    * SSL Terminator
1. Recap  

--- 
# Facts about nginx 
* pronounced "engine-x" 
* A web server, reverse proxy and load balancer 
* First developed in 2004 by Igor Sysoev 
* Designed to solve the C10K Problem[^1]

[^1]: Concurrently handling ten thousand connections

---
# Moar Facts about nginx 
* Open Source nginx and nginx Plus
* nginx powers 1.84 million domains and now serves 28.5% active websites.[^2]
    * Apache is 2nd with 27.8% websites

[^2]: [Netcraft April 2020 Web Server Survey](https://news.netcraft.com/archives/category/web-server-survey/)

--- 
Q: How do I know which webserver serving my content? 

--- 

Q: How do I know which webserver serving my content? 
A: Look a the http response headers using your browser's dev tools.

---




--- 

# Setup 
* Digital Ocean Droplet 
* Dockerized Node.js apps 



--- 
When you install nginx, the installator will put your config file somewhere like `/etc/nginx/sites-available/default` (digital ocean)

proxy_pass directive    


Reverse Proxy Server 
```
server {
    listen 80;

    server_name nodejs-server;

    location / {
        proxy_pass http://167.172.126.205:8080/;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}
```




the response headers tell you the server! 



--- 


Recap 

--- 
![left 90%](https://media.giphy.com/media/3oz8xuflXVQerHqDCM/giphy.gif)

## kimschlesinger.com
## @kimschles
