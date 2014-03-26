# ansible-gridracer

Quickly setup your Raspberry Pi for [gridracer](https://github.com/scottmotte/gridracer).

## Installation

```
git clone https://github.com/scottmotte/ansible-gridracer.git
cd ansible-gridracer
cp hosts.example hosts
cp wpa_supplicant.conf.example wpa_supplicant.conf
cp .ngrok.example .ngrok
```

Edit the `wpa_supplicant.conf` and `hosts` files.

Deploy using [ansible](http://www.ansibleworks.com). (install instructions for ansible are in [requirements](#requirements) below.

```
ansible-playbook playbook.yml -i hosts --ask-pass --sudo -c paramiko
```

## Requirements

[Ansible](http://www.ansibleworks.com/) is required. 

### Installing Ansible on Mac

```
cd /tmp
git clone git://github.com/ansible/ansible.git
cd ./ansible
git checkout v1.4.3
sudo make install
sudo easy_install jinja2 
sudo easy_install pyyaml
sudo easy_install paramiko
```

## History

This project was originally built when trying to control an RC Car with a Raspberry Pi. 

## Issues

If you run into issues with python.

```
sudo apt-get install python-apt --fix-missing
```


