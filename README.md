# Mosquitto Authentication Plugin: MySQL with Redis Cache

This authentication plugin for Mosquitto uses MySQL as the primary data store and Redis as a caching layer to optimize authentication and ACL checks.


## Features:

1.  Authenticates MQTT clients using user credentials stored in MySQL.
2.  ACL (Access Control List) checks for MQTT topics based on data stored in MySQL.
3.  Caches credentials and ACLs in Redis for faster subsequent checks.

## Prerequisites:

-   Mosquitto MQTT Broker
-   MySQL Server.
-   Redis Server

## Configuration:

Add the following lines to your `mosquitto.conf`:

    auth_plugin /path/to/your/plugin.so
    auth_opt_redis_url redis://localhost:6379
    auth_opt_mysql_host localhost
    auth_opt_mysql_db mqttacl
    auth_opt_mysql_user your_mysql_user
    auth_opt_mysql_pass your_mysql_password

Replace paths and connection details to match your setup.

## Contribute:
Feel free to fork this repository, create a feature branch, and submit a pull request for any enhancements or bug fixes.
