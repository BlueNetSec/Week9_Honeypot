# Week9_Honeypot
Time spent: **19** hours spent in total
> Objective: Setup a basic honeypot and provide a working demonstration of its effectiveness at detecting or collecting data about an attack.

## Set up
- [ ] First, I was trying the follow the instructions provided on the assignment page. But I stuck at milestone 1. I was not able to create the VM using the given command:
" gcloud compute instances create "mhn-admin" --machine-type "f1-micro" --subnet "default" --maintenance-policy "MIGRATE"  --scopes "https://www.googleapis.com/auth/devstorage.read_only","https://www.googleapis.com/auth/logging.write","https://www.googleapis.com/auth/monitoring.write","https://www.googleapis.com/auth/servicecontrol","https://www.googleapis.com/auth/service.management.readonly","https://www.googleapis.com/auth/trace.append" --tags "mhn-admin","http-server","https-server" --image "ubuntu-1404-trusty-v20171010" --image-project "ubuntu-os-cloud" --boot-disk-size "10" --boot-disk-type "pd-standard" --boot-disk-device-name "mhn-admin""

![error](https://user-images.githubusercontent.com/24555370/32417666-c936e120-c22a-11e7-8d26-965e89e07561.PNG)

## Alternative
- [ ] After research online, I discover that thereare a list of honeypots tools aviable online. So I decided to use KFSensor to do this assignment. KFSensor has a 30-day free trial, which is more than enough for this week's assignment. In addition, I also use the Wireshark  and WinPcap, the industry standard network packet capture library.

-[ ] After setting up KFSensor:
![event](https://user-images.githubusercontent.com/24555370/32418119-f34e9780-c231-11e7-9c7e-f755568c291d.PNG)

![attack](https://user-images.githubusercontent.com/24555370/32418153-61224d10-c232-11e7-907f-2d6d6a21461a.PNG)

![track event](https://user-images.githubusercontent.com/24555370/32418154-68571548-c232-11e7-908b-faefa6febad3.PNG)  

## Finding the vulnerabilities in this honeyspot
- [ ] select one of visitor's ip address: 162.125.34.137 
- [ ] use Nikto to scan against this ip ./nikto.pl -h 162.125.34.137 
![niko](https://user-images.githubusercontent.com/24555370/32418229-ce0b4156-c233-11e7-9878-42ddd2b71241.PNG)

## Banner grabbing using netcat
- [ ] nc  162.125.34.137 80
- failed banner grabbing, not able to connect to the port
![failed](https://user-images.githubusercontent.com/24555370/32418311-64951c72-c235-11e7-87a2-a1744fbcb6ab.PNG)


