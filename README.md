## PHP 7.3 fork

This is a fork of DockPressDebug from Threenine.co.uk: https://github.com/threenine/dockpressdebug

Before running docker-compose, it's necessary to build a custom image. You can use the following command:

`docker build -t wordpressdebugcustom:php7.3 .
`

Also, in docker-compose.yaml, find the following line and put there your ip to be able to use the debugger:
`
XDEBUG_CONFIG: remote_host={your ip}       # Insert the IP of your host machine
`

###Enjoy!

# DockPressDebug

Adds xDebug support to the WordPress container for Docker.

Removes  opcache configuration file that the WordPress image installs because it appeared to affect PHP Opcode Caching . 

This is primarily targeted for local development environments and should not be used for PRODUCTION environments

For full details  on how to use this check [Docker and Wordpress debug environment](https://threenine.co.uk/docker-wordpress-debug-environment/)
