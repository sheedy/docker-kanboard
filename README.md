# Kanboard

Based on [Kanboard for Docker](https://github.com/fguillot/kanboard/blob/master/docs/docker.markdown)

I just added the `gd` library and used `php5enmod` to enable it. I also removed the `EXPOSE 80` as I am using [jwilder/nginx-proxy](https://github.com/jwilder/nginx-proxy) to dynamically add hosts/ports.


Build your own Docker image
---------------------------

From your kanboard directory run the following command:

```bash
docker build -t youruser/kanboard:master .
```

To run your image in background on the port 80:

```bash
docker run -d --name kanboard -p 80:80 -t youruser/kanboard:master
```

Store your data on a volume
---------------------------

You can also save your data outside of the container, on the local machine:

```bash
docker run -d --name kanboard -v /your/local/data/folder:/var/www/html/data -p 80:80 -t youruser/kanboard:master
```
