Nginx Role
=========

Installs nginx via `apt`. Option to install nginx from source when nginx_custom_modules is set.
(This role will not install custom module dependencies)

Role Variables
--------------

```
nginx_custom_settings:
  server_names_hash_bucket_size: 64
  map_hash_bucket_size: 64
  
# suggested custom module use
nginx_custom_modules:
  - name: nginx_http_geoip2_3.2
    source: https://github.com/leev/ngx_http_geoip2_module/archive/3.2.tar.gz
    pkgname: ngx_http_geoip2_module-3.2
    file: ngx_http_geoip2_module.so

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