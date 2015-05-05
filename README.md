# Kanboard

Based on [Kanboard for Docker](https://github.com/fguillot/kanboard/blob/master/docs/docker.markdown)

I just added the gd library and used php5enmod to enable it. I also removed the `EXPOSE 80` as I am using [jwilder/nginx-proxy](https://github.com/jwilder/nginx-proxy) to dynamically add hosts/ports.
