# ansible-role-simple-nginx
Simple ansible role for provising a nginx installation with the following features:

* host one virtual site with one document root and/or one reverse proxy
* configure user access to document root
* configure ssl with self signed certificate - NEVER USE THIS FOR PRODUCTION SERVICES!
* redirect port 80 requests to 443
* configure basic auth authentication

The followingen variables are used:

* nginx_document_root_user: Optional, unix user with write access to /var/www/html
* nginx_document_root_group: Optional, unix group with write access to /var/www/html
* nginx_document_root_uri: Optional relativ URI path to document root. If not set, no location for static content will be created.
* nginx_proxy_uri: Optional relativ URI path to service, default is undefined and no proxy service will be installed
* nginx_proxy_service_url: Optional service URL, default is undefined and no proxy service will be installed
* nginx_access_user: Optional, basic authentication user name
* nginx_access_password: Optional, basic authentication password
* nginx_access_area_name: Optional, basic authentication area name
