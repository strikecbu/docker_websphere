What is it
==========

build docker websphere bind with sqlserver


how to run
==========

	docker run --name testweb2 -p 9043:9043 -p 9443:9443 -p 7777:7777 -v [yourFolder/]:/opt/IBM/WebSphere/AppServer/profiles/AppSrv01/installedApps/ -v [yourFolder/]:/opt/IBM/WebSphere/AppServer/profiles/AppSrv01/logs/  -v [yourFolder/]:/opt/IBM/WebSphere/AppServer/profiles/AppSrv01/D/  --link sqlserver:sqlserver  andychentw/websphere8.5

first -v : place apps locate place build in WAS \n
second -v : WAS system log folder \n
third -v : for project in windows, link D:/ to this \n

WAS settings
===============
user: wsadmin \n
password: p@ssw0rd \n

SQL server settings
===================
host: sqlserver \n
user: sa \n
password: p@ssw0rd \n



