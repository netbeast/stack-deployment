# netbeast-stack-ansible

It's a complete Ansible Playbook faced on NB stack deployment.
Introduce the IP address of your server in ```hosts```file.

Copy ssh key in the server by typing 
```ssh-copy-id USER@IP_ADDRESS```
*You need to have your public key in ```~/.ssh/authored_keys```before doing it.

Once you've copied ssh keys, you can start executing tasks!

```ansible-playbooks -i hosts site.yml```

You must prepare Netbeast website source code in the correct location:

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

Remember to change ```hosts``` file with the correct IP
