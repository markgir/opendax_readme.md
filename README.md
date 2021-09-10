# Deploy opendax peatio exchange in bash scripts

# installation

# ubuntu 20.04 

upgrade your system:
```
sudo apt update
sudo apt upgrade
```

create user :
```

sudo adduser app

sudo usermod -a -G sudo app
```
install ruby:
```
sudo apt install ruby-full

```
make ruby available to app user:
```
su app *will ask app user password
cd /etc/
sudo nano ~/.bashrc
[[ -s /usr/local/rvm/scripts/rvm ]] && source /usr/local/rvm/scripts/rvm  *** on the end of the file
```

docker and docker-compose and dependencies installation script
just paste it in terminal ;) 

while install this script it will ask you app password

```
bash <(curl -Ls https://gist.githubusercontent.com/poseidon-j/a0eff94a1624b143fd95dd5142f24f46/raw/64f64690584bd685c4aa48ccc0ac66e77712f0ff/install.sh)
```
please login to app user
 ```
 su - app
 ```
 
 clone opendax 
 ```
 https://github.com/poseidon-j/opendax.git
 
 cd opendax
 ```
 
Install ruby bundler 
```
gem install bundler

bundle

```
```sudo nano config/app.yml```

and change credentials like domain and subdomain
example: http://ex.example.com

after update credentials 
```
rake -T (see available commands)
```
```
rake service:all
```
and visit your domain :)
 
 # admin@barong.io is superadmin
```
Seeded users:
Email: admin@barong.io, password: 0lDHd9ufs9t@ 

Email: john@barong.io, password: Am8icnzEI3d!
```

