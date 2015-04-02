# Daux.io Dockerfile

This Dockerfile will download the latest version of daux.io and will deploy it on a apache-php container.

## Usage
````
docker pull nicolasritouet/daux.io
docker run -d -p 80:80 nicolasritouet/daux.io
````

You can now test the deployment:
````
curl http://localhost
````


## To fix
- add htaccess to have clean urls
- add a volume for the /docs folder
- add nginx (??)
- improve documentation
