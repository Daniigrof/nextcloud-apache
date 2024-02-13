# nextcloud-apache
Implement Nextcloud-Apache on running app with nginx proxy server

Nextcloud filesharing platform has tow types of implementations
  1. nextcloud-php
  2. nextcloud-apache

To deploy "nextcloud-php" on your running app can be a little challenging,
You have to set on your existing nginx server many specific settings,
and set it on PHP. 

Unlike the second option "nextcloud-apache",
This option gives you the opportunity to deploy nextcloud with all packages.
Witch means - with apache proxy server and PHP inside.

The settings you would have to change are the two proxy servers ports.

In this guide we set the nginx server (existing on our running app) to default port: 80
And for the Apache server, change the port to: 8080
Every http://my-app/nextcloud API request forwards via nginx to apache server (inside the nextcloud containner).

