What is it
==========

build docker websphere bind with sqlserver


how to run
==========

	docker run --name testweb2 -p 9043:9043 -p 9443:9443 -p 7777:7777 -v [yourFolder/]:/opt/IBM/WebSphere/AppServer/profiles/AppSrv01/installedApps/ -v [yourFolder/]:/opt/IBM/WebSphere/AppServer/profiles/AppSrv01/logs/  -v [yourFolder/]:/opt/IBM/WebSphere/AppServer/profiles/AppSrv01/D/  --link sqlserver:sqlserver  andychentw/websphere8.5

first -v : place apps locate place build in WAS
second -v : WAS system log folder
third -v : for project in windows, link D:/ to this

WAS settings
===============
user: wsadmin
password: p@ssw0rd

SQL server settings
===================
host: sqlserver
user: sa
password: p@ssw0rd



