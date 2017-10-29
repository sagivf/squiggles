

## CMD
- kill process `ps aux | grep node -> kill -9 16783` 
- find process by port and kill: `lsof -n -i4TCP:[PORT] | grep LISTEN | awk '{ print $2 }' | xargs kill`
- https://til.hashrocket.com/posts/e4c8c665a8-find-and-kill-all-processes-listening-on-a-port

## Mongo
```
- 3.2.10 version
- sudo service mongod start

/lib/systemd/system/mongod.service 
in /etc/mongod.conf

https://docs.mongodb.com/v3.2/tutorial/install-mongodb-on-ubuntu/
/var/log/mongodb/mongod.log
```

## Pin a specific version of MongoDB
```
* echo "mongodb-org hold" | sudo dpkg --set-selections
* echo "mongodb-org-server hold" | sudo dpkg --set-selections
* echo "mongodb-org-shell hold" | sudo dpkg --set-selections
* echo "mongodb-org-mongos hold" | sudo dpkg --set-selections
* echo "mongodb-org-tools hold" | sudo dpkg --set-selections    
```

## Node
- nodemon --debug=3002 server.js

## NPM
- npm ls --depth 0
- ntl	
- npm run env
- npm run env | grep npm_

## Heroku
- heroku repo:purge_cache --app appName


## BackUP:
- sudo dd if=/dev/sda1 of=/media/sagivf/Miri/ddbackup/back.img
- sudo kill -USR1 PID; sleep 1; ## show progress - PID use top
- df -BG ## show sizes


## Ubuntu
* sudo apt-get update
* sudo apt-get upgrade
* sudo apt-get dist-upgrade


## GIT
* git config credential.helper store
* https://git-scm.com/docs/git-credential-store

ab -c200 -t10 http://localhost:8080/
benchmark