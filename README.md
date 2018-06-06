Nginx Role
=========


Role Variables
--------------

```
# Any Vars?

nginx_sendfile: "on"
nginx_max_body_size: "10M"
nginx_listen_port: 80

fastcgi_buffers: "8 16k"
fastcgi_buffer_size: "32k"
fastcgi_connect_timeout: 300
fastcgi_send_timeout: 300
fastcgi_read_timeout: 300


```

----------------

```
# requirements.yml

- src: https://github.com/ergontech-ansible-roles/nginx
  version: master
  name: nginx
```

License
-------

[MIT](LICENSE)