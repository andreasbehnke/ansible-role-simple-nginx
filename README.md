# ansible-role-simple-nginx
Simple ansible role for provising a nginx installation with the following features:

* host one virtual site with one document root
* configure user access to document root
* configure ssl with self signed certificate - NEVER USE THIS FOR PRODUCTION SERVICES!
* redirect port 80 requests to 443
* configure basic auth authentication

The followingen variables are used:

* nginx_document_root_user: Unix user with write access to /var/www/html
* nginx_document_root_group: Unix group with write access to /var/www/html
* nginx_access_user: Optional, basic authentication user name
* nginx_access_password: Optional, basic authentication password
* nginx_access_area_name: Optional, basic authentication area name