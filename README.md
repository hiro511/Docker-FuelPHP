# Docker-FuelPHP
Docker Image packaging for FuelPHP

## Create a Dockerfile in your FuelPHP project

``` dockerfile
FROM hiro511:fuelphp

ONBUILD COPY your_project/app /var/www/html/fuel/fuel

```
Then, run the commands to build and run the Docker image:

``` bash
docker build -t your-fuelphp-app .
docker run -itd -p 80:80 -name fuel your-fuelphp-app

```


If you want to mount your project, the folloing commands is available.

```
docker run -itd -p 80:80 --name fuel -v your-fuelphp-project/app:/var/html/www/fuel/fuel/app .
```
