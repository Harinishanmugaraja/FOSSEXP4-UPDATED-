PROJECT SETUP
npm install
node index.js

DATABASE
Open MongoDB Compass
Create new Database named as taskdb
create collection named as tasks

COMMANDS FOR DEPLOYMENT
Open Ubuntu/WSL
sudo apt update
sudo apt install ansible -y
ansible --version
cd /mnt/c/Users/<YourWindowsUsername>.....GET INTO YOUR PROJECT FOLDER(Diskname should be in lowercase and use forward slash)
ansible-playbook deploy.yml



