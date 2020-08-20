
### 修改 Homestead.yaml
```
ip: "192.168.10.10"
memory: 1024
cpus: 1
provider: virtualbox

authorize: ~/.ssh/id_rsa.pub

keys:
    - ~/.ssh/id_rsa

folders:
    - map: ~/code
      to: /home/vagrant/code
      type: "nfs"

sites:
    - map: homestead.test
      to: /home/vagrant/code/laravel/public
    - map: larabbs.test
      to: /home/vagrant/code/larabbs/public

databases:
    - homestead
    - larabbs
```
- vagrant provision && vagrant reload

### 修改composer.json 
- composer dump-autoload

###
```
yarn add ***** --no-bin-links 
yarn install ***** --no-bin-links 
npm install ***** --no-bin-links 
```
