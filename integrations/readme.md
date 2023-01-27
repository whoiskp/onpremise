### Why?
- This project use for customize sentry simple version [self-hosted](https://github.com/whoiskp/onpremise) - v9.1.2

### Coding & update
1. Exec to container:
```docker exec -it <sentry-web-container-name> bash```
2. Install tools:
```sh
apt-get update & apt-get install -y vim
```
3. Update file with new logic then copy this change to same path in folder:
- path: ```/usr/local/lib/python2.7/site-packages/sentry/integrations```
```sh
cp /mnt/<path-plugin>/<file-change-name>.py /usr/local/lib/python2.7/site-packages/sentry/integrations/<path-plugin>/<file-change-name>.py 
```
4. restart ```docker-compose restart``` to apply change
 