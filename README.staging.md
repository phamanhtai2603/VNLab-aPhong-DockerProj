### 1. 環境の準備

```
# get source ansible playbook
git clone https://github.com/phongnx1/ansible-docker-training.git

# checkout staging
git checkout staging

# get source application
cd ansible-playbook
git clone https://github.com/phongnx1/yii2-project.git

# create log dir
cd yii2-project
mkdir log

cd ansible-playbook
ansible-playbook -i hosts.staging provision.yml --become

# install mysql by docker-compser
ansible-playbook -i hosts.staging install_mysql.yml --become

# install nginx-php-fpm by docker-compser
ansible-playbook -i hosts.staging deploy_app.yml --become

#Confirm start web: Browser
```
