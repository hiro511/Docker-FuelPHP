# Docker-FuelPHP
Docker Image packaging for FuelPHP

## Docker pull command
```
docker pull hiro511/fuelphp
```

## Start a FuelPHP project simply
```
docker run -d -p 80:80 --name fuel -v your-fuelphp-project/app:/var/www/html/fuel/fuel/app hiro511/fuelphp
```


## Create a Dockerfile in your FuelPHP project

``` dockerfile
FROM hiro511/fuelphp

ONBUILD COPY your_project/app /var/www/html/fuel/fuel

```
Then, run the commands to build and run the Docker image:

``` bash
docker build -t some-fuelphp .
docker run -d -p 80:80 -name fuel some-fuelphp

```


If you want to mount your project, the folloing commands is useful.

```
docker run -d -p 80:80 --name fuel -v your-fuelphp-project/app:/var/www/html/fuel/fuel/app some-fuelphp
```
