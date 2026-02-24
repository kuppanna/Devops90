# Check running processes

 ps aux : Shows all running processes with CPU, memory, and user details.
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0   1756   812 pts/0    Ss   02:05   0:00 sh
root          63  0.0  0.0   3280  1768 pts/0    R+   07:07   0:00 ps aux

# Capture a small troubleshooting flow
Check service status
 root@ip-172-31-26-245:/home/ubuntu# systemctl is-active nginx : active

# Network connectivity check
 
 netstat -tunlp | grep nginx 
  root@ip-172-31-26-245:/home/ubuntu# netstat -tunlp | grep nginx
tcp        0      0 0.0.0.0:80              0.0.0.0:*               LISTEN      1775/nginx: master  
tcp6       0      0 :::80                   :::*                    LISTEN      1775/nginx: master  

# Log inspection

Nginx logs are usually located in:

root@ip-172-31-26-245:/home/ubuntu# cat /var/log/nginx/access.log
::1 - - [24/Feb/2026:08:05:11 +0000] "GET / HTTP/1.1" 200 615 "-" "curl/8.5.0"
root@ip-172-31-26-245:/home/ubuntu# tail -f /var/log/nginx/access.log
::1 - - [24/Feb/2026:08:05:11 +0000] "GET / HTTP/1.1" 200 615 "-" "curl/8.5.0"
::1 - - [24/Feb/2026:08:11:25 +0000] "GET / HTTP/1.1" 200 615 "-" "curl/8.5.0"

# Resource utilization check using below command 
  top
  htop
  free -m
  df -h


# Configuration validation
root@ip-172-31-26-245:/home/ubuntu# nginx -t 
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful