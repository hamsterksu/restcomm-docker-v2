# restcomm-docker-v2

NOTE: it's concept

Split Restcomm-Docker image to 5 images

1. restcomm/baseimage:java7 - 861 MB
2. restcomm/base:as7 - 1.127 GB
3. restcomm/restcomm:as7 - 1.182 GB
4. restcomm/olympus:as7 - 1.14 GB
5. restcomm/rvd:as7 - 1.5 GB

Containers' update size

- restcomm  ~ 55 MB
- olympus - 13 MB
- rvd - 23 MB

### restcomm/baseimage:java7
Install java7 and other packages

### restcomm/base:as7
jboss + sip-servlets + webrtc + tools

### Issues
1. Suitable for distributed env
2. Need to use docker compose to run env
3. for one host - need to start a few AS on the same machine, SOLUTION - all-in-one container 
