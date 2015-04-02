# Daux.io Dockerfile

This Dockerfile will download the latest version of daux.io and will deploy it on a apache-php container (thx tutum.co)

## Usage
````
docker run -d -p 80:80 -v /home/user/docs:/var/www/html/docs inanimate/daux.io
````

You can now test the deployment:
````
curl http://localhost
````


## Notes

* A default config.json, which needs to reside in your docs/ directory, is included and if no volume is bind mounted, automatically added (via Dockerfile).
* The clean_urls option doesn't seem to work (makes the path look like `http://localhost/Welcome` instead of `http://localhost/index.php/Welcome`, even with `AllowOverride` set to `All`. Not sure what that's about but if someone figures out whats going on, send me a pull req.
