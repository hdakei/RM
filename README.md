# RM Project

> Dockerize NGINX with Varnish cache and php-fpm with:
> Mysql ,Redis, elasticsearch and rabitmq

![Image of Hazhir](https://i.ibb.co/JtmJFq2/image.jpg "RMI")

 Dockerfiles :
- [x] Nginx,Varnish and php-fpm
- [ ] Mysql ,Redis, elasticsearch and rabitmq
>Mysql ,Redis, elasticsearch and rabitmq don't have dockerfile yet but I'll update them as soon as possible
    
# Setup and Use
*This application will be able to run on every platform like Linux, Mac, and Windows. we are going to set up this application in the server has docker :*

**Setup by docker-compose**


>Please install docker-compose if you don't have it in your machine.

*You have to run command in the project's directory as following;

> #---< run application by Docker-compose >---#

```
docker-compose up -d --build
```

~~---------------------------------~~

**backup project**
>This project is for backup from mysql database to current directory.
>also auto delete backup before 7 days
*You could change the directory and time for keeping backup in the code*

**CRON**
>you have to set the following command in your crontab via crontab -e

```
30 0 * * * [Directory of project]/backup/backup.sh
```
>remember to give the backup.sh execute attribute via chmod +x

**For Restore **
```
gunzip < [backupfile.sql.gz] | mysql -u [uname] -p[pass] [dbname]
```

~~---------------------------------~~

I will add gitlab-ci and k8s for this project...
