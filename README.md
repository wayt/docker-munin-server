# docker-munin-server

Run the server 

* `docker run -p 8080:80 -d -v /path/to/conf.d:/etc/munin/munin-conf.d -v /path/to/access:/etc/munin-access --name munin-server maxwayt/munin-server`

To manage create the htpasswd file

* `htpasswd -c /path/to/access/htpasswd username`

To manage your nodes (See [https://github.com/Wayt/docker-munin-node](https://github.com/Wayt/docker-munin-node)) create a configuration file

* `vim /path/to/conf.d/node-1.conf`

Example configuration
```
[fii.foo.com]
    address foo
    use_node_name yes
```
