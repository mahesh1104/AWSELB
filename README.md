# AWSELB
Types of load balancer
   Classic load balancer
     Designed for EC2-classic network
     Not recommended for VPC       
   applicaton laod balancer
     HTTP and HTTPS traffic
     Terminates the client connection
     TCP ports 1-65535
     Listener supports IPv6
     Path and host-based routing
   networker load balancer
     Supports any TCP connection
     Layer 4 load balancer
     Handles high traffic at low latency 
     Does not terminate HTTP(S) Connections 
   thired party laod balancer - Fi load balancer.
   
Load-balancing applications
Sercuring your applications using https
Path-based routing for containers
sticky sessions and idle timeouts
Implementing load-balancing with IPv6
-----------------------------------------------

Lab setup
Manual or powershell script 

VPC:webapp-vpc
   - CIDR:172.32.0.0/16
   - Enable DNS hostnames
   - Internet gateway:webapp-igw

Subnets:
   - web-1a: 172.31.1.0/24
   - web-1b: 172.31.2.0/24
   - app-1a: 172.31.101.0/24
   - app-1b: 172.31.102.0/24
  
Routes
Route table: webapp-rt
   - Associate with all subnets

Default routes:
   - IPv4:0.0.0.0/0
   - IPv6: ::0/0
   - Target: webapp-igw
---------------------------------------------
github.com/benpiper/aws-powershell
---------------------------------------------

Load Balancing Internet-facing HTTP-based Web Applications

