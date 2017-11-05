# Week9_Honeypot
Time spent: **19** hours spent in total
> Objective: Setup a basic honeypot and provide a working demonstration of its effectiveness at detecting or collecting data about an attack.

## Set up
- [] First, I was trying the follow the instructions provided on the assignment page. But I stuck at milestone 1. I was not able to create the VM using the given command:
" gcloud compute instances create "mhn-admin" --machine-type "f1-micro" --subnet "default" --maintenance-policy "MIGRATE"  --scopes "https://www.googleapis.com/auth/devstorage.read_only","https://www.googleapis.com/auth/logging.write","https://www.googleapis.com/auth/monitoring.write","https://www.googleapis.com/auth/servicecontrol","https://www.googleapis.com/auth/service.management.readonly","https://www.googleapis.com/auth/trace.append" --tags "mhn-admin","http-server","https-server" --image "ubuntu-1404-trusty-v20171010" --image-project "ubuntu-os-cloud" --boot-disk-size "10" --boot-disk-type "pd-standard" --boot-disk-device-name "mhn-admin""

![error](https://user-images.githubusercontent.com/24555370/32417666-c936e120-c22a-11e7-8d26-965e89e07561.PNG)

