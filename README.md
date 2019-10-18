# angular_build_issues
npm ERR! No Space left on device

have a docker file , when i run npm install i face this issue "npm ERR! No Space left on device"
docker must be light weight but when i ran
"sudo du -sh /var/lib/docker" 
i got result as 

"5.4G    /var/lib/docker"
ie 5.4 gb is used by docker that there is no more place left.

i  removed all images and containers thro

"docker system prune --all --force --volumes"

now when i ran 
"sudo du -sh /var/lib/docker" 
"827M    /var/lib/docker"

sudo ls -l /var/lib/docker
total 12
drwx------  2 root root   24 Oct 14 02:54 builder
drwx------  4 root root   92 Oct 14 02:54 buildkit
drwx------  3 root root   20 Oct 14 02:54 containerd
drwx------  2 root root    6 Oct 18 06:14 containers
drwx------  3 root root   22 Oct 14 02:54 image
drwxr-x---  3 root root   19 Oct 14 02:54 network
drwx------ 12 root root 8192 Oct 18 06:14 overlay2
drwx------  4 root root   32 Oct 14 02:54 plugins
drwx------  2 root root    6 Oct 18 05:38 runtimes
drwx------  2 root root    6 Oct 14 02:54 swarm
drwx------  2 root root    6 Oct 18 06:14 tmp
drwx------  2 root root    6 Oct 14 02:54 trust
drwx------  2 root root   25 Oct 14 04:00 volumes


