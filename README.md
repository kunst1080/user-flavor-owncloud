user-flavor-owncloud
===

This is a user-flavor for "jail-deploy".
(https://github.com/kunst1080/jail-deploy)

This flavor build a Jail environment for owncloud server.
(http://owncloud.org)

## Getting Started
1. Install jail-deploy
  ```bash
  git clone -b v0.1 git://github.com/kunst1080/jail-deploy.git
  ```

2. Get this user-flavor
  ```bash
  git clone git://github.com/kunst1080/user-flavor-owncloud.git
  ```

3. Create a Jail environment with jail-deploy.
  ```bash
  jail-deploy -4 xxx.xxx.xxx.xxx -f user-flavor-owncloud -y P PRISONER_ROOT_PASSWORD -u PRISONER_USER -p PRISONER_PASSWORD JAIL_NAME
  ```

4. Create a htpasswd file.
  ```bash
  qjail console JAIL_NAME
  htpasswd -c /root/htpasswd USERNAME
  service apache24 restart
  ```
