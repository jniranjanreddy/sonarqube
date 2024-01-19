# sonarqube
## Source: https://linux.how2shout.com/install-sonarqube-on-ubuntu-20-04-18-04-server/
## https://www.fosstechnix.com/how-to-install-sonarqube-on-ubuntu-20-04/  - 9.9
## wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.0.65466.zip

## Notes
```

```



## Kernel parameters are important

root@devops-VirtualBox:/opt/sonarqube/logs# sysctl -a | egrep -i "fs.file-max|vm.max_map_count"
fs.file-max = 9223372036854775807
vm.max_map_count = 524288



## Troubleshooting
```
If it failes to start check logs under
root@devops-VirtualBox:/opt/sonarqube/logs# pwd
/opt/sonarqube/logs
root@devops-VirtualBox:/opt/sonarqube/logs# ll
total 108
drwxr-xr-x  2 sonarh2s sonarh2s  4096 Dec  5 00:51 ./
drwxr-xr-x 11 sonarh2s sonarh2s  4096 Jul 27  2021 ../
-rw-r--r--  1 sonarh2s sonarh2s 13981 Dec  5 00:52 access.log
-rw-r--r--  1 sonarh2s sonarh2s  8122 Dec  5 10:24 ce.log
-rw-r--r--  1 sonarh2s sonarh2s 20430 Dec  5 10:24 es.log
-rw-r--r--  1 sonarh2s sonarh2s    88 Jul 27  2021 README.txt
-rw-r--r--  1 sonarh2s sonarh2s 11231 Dec  5 10:24 sonar.20231205.log
-rw-r--r--  1 sonarh2s sonarh2s 34033 Dec  5 10:24 web.log

```
![image](https://github.com/jniranjanreddy/sonarqube/assets/83489863/4fe89ab1-9686-4d36-8c93-e7c11433d750)


## How to add report generator
```
This was tested for version 9.9
download below jar under /opt/sonarqube/extensions/plugins and restart service
wget https://github.com/cnescatlab/sonar-cnes-report/releases/download/4.2.0/sonar-cnes-report-4.2.0.jar
```
![image](https://github.com/jniranjanreddy/sonarqube/assets/83489863/ad0e75b9-98b0-4db8-9d58-07811020e738)




