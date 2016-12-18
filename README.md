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
spassword: p@ssw0rd

SQL server settings
===================
host: sqlserver 
user: sa 
password: p@ssw0rd

WAS files loacation
===================
如果要變更SQL server的連線設定，或是WAS Debugger mode設定

Microsoft JDBC Driver path ver maping 
-------------------------------------
	/opt/IBM/WebSphere/AppServer/profiles/AppSrv01/config/cells/DefaultCell01/nodes/DefaultNode01/servers/server1/variables.xml
Datasource settings
-------------------
	/opt/IBM/WebSphere/AppServer/profiles/AppSrv01/config/cells/DefaultCell01/nodes/DefaultNode01/servers/server1/resources.xml
Login DB user settings
----------------------
	/opt/IBM/WebSphere/AppServer/profiles/AppSrv01/config/cells/DefaultCell01/security.xml
WAS debugger mode settings
--------------------------
/opt/IBM/WebSphere/AppServer/profiles/AppSrv01/config/cells/DefaultCell01/nodes/DefaultNode01/servers/server1/server.xml




