# netbeast-stack-ansible

It's a complete Ansible Playbook faced on NB stack deployment.
It only needs to execute the following commands:
```
cd ~/deploy/server
git clone WEBSITE_REPO
mv WEBSITE_REPO src
cd src
sudo npm install
```

You must change the ``` Copy certs``` tasks in ```nginx/tasks/main.yml``` file
according to the current location of your certs.
