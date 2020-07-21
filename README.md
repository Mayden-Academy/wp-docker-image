# wp-docker-image

Start by creating the following directory

```
~/sites/wordpress
```

You may need to sudo this command. Once created set the permissions for the sites directory:

```
sudo chmod -R 777 ~/sites
```

Now we need to clone this repo into that directory, run the following command from the academyServer directory

```
git clone git@github.com:Mayden-Academy/wp-docker-image.git .
```

You can now turn the image on by running:

```
docker-compose up
```

This will take a minute or two to run, once done it should finish on something that looks like the below:

```
db_1     | Version: '5.7.26'  socket: '/var/run/mysqld/mysqld.sock'  port: 3306  MySQL Community Server (GPL)
```

You should now be able to load [http://localhost:8000/](http://localhost:8000/) in your browser and see the WordPress install page.

Provided you see the install, now press ctrl+c on the running docker image. This will gracefully shut down your image.

To run your docker image in the background you can run:

```
docker-compose up --detach
```

You can now put all your application files in:
```
~/sites/wordpress/html
```

To shutdown your box run:
```
docker-compose down
```
