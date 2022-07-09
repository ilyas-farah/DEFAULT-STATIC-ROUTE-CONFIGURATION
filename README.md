# DEFAULT-STATIC-ROUTE-CONFIGURATION
Default Static Route
--------------------
R1
----
int g0/1
ip address 192.168.1.1 255.255.255.0
no shutdown 
int g0/0
ip address 12.0.0.1 255.255.255.252
no shutdown 

Loopack
---------
R2
----
int g0/0
ip address 12.0.0.2 255.255.255.252
no shutdown 
int lo1
ip address 10.1.1.1 255.255.255.0
int lo2
ip address 10.1.2.1 255.255.255.0
int lo3
ip address 10.1.3.1 255.255.255.0
int lo4
ip address 10.1.4.1 255.255.255.0
int lo5
ip address 10.1.5.1 255.255.255.0
show ip route connected

Default Static Route
--------------------
R1
-----
ip route 0.0.0.0 0.0.0.0 12.0.0.2
![Default Static Routing](https://user-images.githubusercontent.com/106605770/178120409-442de5cb-0dea-4f19-bdb2-c1f022311122.PNG)
