# Static Site with SSL

With a couple of Docker containers you can "easily" spin up a static site server with self managed SSL certs.  I put easily in quotes because the docker commands to set this up are long and I can never remember them. So I put those commands in an "easy" (I hope) to use script. 

## Get started
```
# Set up your site. 
git clone https://github.com/rjsteinert/serve-a-static-site-with-ssl-example.git my-site 
cd my-site 
# Add your static folder and a hello world.
mkdir public
echo "Hello World" > public/index.html
# Configure for which domain you will generate SSL certs for.
cp config.defaults.sh config.sh
vim config.sh
# Start it up.
./start.sh
```

## Pointers
- I've seen getting the SSL certs take a couple of minutes one time and then another where it didn't seem to work but after running start.sh again it worked right away :P.


## Credits
- https://hub.docker.com/r/jrcs/letsencrypt-nginx-proxy-companion/
- https://hub.docker.com/r/jwilder/nginx-proxy
- https://hub.docker.com/_/nginx
