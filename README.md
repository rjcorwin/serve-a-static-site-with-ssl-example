# Static Site with SSL

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
