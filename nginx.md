footer: @kimschles

## nginx and Node.js 

### Kim Schlesinger

#### Denver Node.js Meetup - May 2020 

--- 

# Agenda 
1. About nginx   
1. Demo setup 
1. nginx as a
    * Reverse Proxy 
    * Web Cache
    * Load Balancer 
    * SSL Terminator
1. Recap  

---
# Kim Schlesinger

![inline](images/kim.png)

--- 
# Agenda 
1. About nginx   



--- 
![inline 20%](https://upload.wikimedia.org/wikipedia/commons/c/c5/Nginx_logo.svg)

--- 
# About nginx 



* pronounced "engine-x" 
* A web server, reverse proxy and load balancer 
* First developed in 2004 by Igor Sysoev 
* Designed to solve the C10K Problem[^1]

[^1]: Concurrently handling ten thousand connections

---
# Moar about nginx 
* Open Source nginx and nginx Plus
* Serves 28.5% active sites on the web![^2]
    * Apache is 2nd with 27.8% websites

[^2]: [Netcraft April 2020 Web Server Survey](https://news.netcraft.com/archives/category/web-server-survey/)

--- 

## Q: How do I know which webserver is serving my content? 
![inline](https://media.giphy.com/media/3o7buirYcmV5nSwIRW/giphy.gif)

--- 

## A: Look a the http response headers using your browser's dev tools.

* Open dev tools
* Go to the network tab
* Refresh the page
* Look at response headers 

---
![80%](/Users/kschlesinger/presentations/images/dev-tools-view.png)


--- 
Something about nginx and node.js 

--- 

Something about JS programming vs. configuration management 

--- 
# Agenda 
1. About nginx   
1. Demo setup 
1. nginx as a
    * Reverse Proxy 
    * Web Cache
    * Load Balancer 
    * SSL Terminator
1. Recap  

---
# Agenda 
1. About nginx   
1. Demo setup
1. nginx as a
    * Reverse Proxy 
    * Web Cache
    * Load Balancer 
    * SSL Terminator
1. Recap  

-- 


# Demo Setup 
* Digital Ocean Droplet 
    * Ubuntu `18.04.3`
* Dockerized Node.js apps 
    * Code at github
    * Docker images at docker hub



--- 
When you install nginx, the installator will put your config file somewhere like `/etc/nginx/sites-available/default`



Reverse Proxy Server 

```
server {
    location / {
        proxy_pass http://<IP_ADDRESS_OF_YOUR_SERVER>:8080/;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}
```




--- 


Recap 

--- 
![left 90%](https://media.giphy.com/media/3oz8xuflXVQerHqDCM/giphy.gif)

## kimschlesinger.com
## @kimschles
