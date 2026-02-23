#  Process Management
ps aux : List all running process  with PID User Time Command 
top : real time porcess monitoring like Memory  CPU Load Porcess 
htop : improved interactive, user-friendly version of top
pidof  ngnix : Get PID of a process
kill  33 : Terminate process by PID
kill -9 33 : Force kill a process
pkill ngnix : Kill process by name
nice -n 10 yes : Start process with priority
renice -n -5 33 : Change running process priority
uptime: Uptime tells how long the system has been continuously running and shows system load.
free -m : System memory is healthy and under no stress
vmstat: vmstat is used for real-time system performance troubleshooting (CPU, memory, swap, I/O)

# File system and logs
pwd : present working dicectory
ls -lh : List files with size in human readable format
cd :  Change directory
mkdir : create directory 
rm -rf : Remove directory recursively
cp -r src dest : copy directiory  from soure to dest
mv src dest : move or rename file
touch test.txt: Create empty file
cat test.txt: View entire file
less test,txt : View large file page by page
head -n 20 test.txt : Show first 20 line 
tail -n 20 test.txt : show last 20 line
grep "name": test.txt: Search text in file
grep -r "text" /dir : Search recursively
find / -name file.txt : fine file by name 
df -h : check disk usage 
du -sh * : shows the disk usage of each directory in human-readable format
chmod 755 file : change the file permission 
chown : change file ownership 
# Networking Troubleshooting
ip addr : show Ip addres of device 
ip route : show routing table
ping www.google.com : check network conncetivity
curl -i https://www.google.com  : command is commonly used to test network connectivity and website availability
wget <url> : Dowbloads the file 
dig google.com : DNS lookup
traceroute google.com : Trace network path
hostname -i : Show system IP address



# System Information
uname -a : Show system information
uptime: show system uptime
free -m : Show memory usage
whoami : show current  user 
id : Show user and group IDs
history : show command history
clear : clear terminal screen 
