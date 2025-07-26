# Genesis

Genesis is a VPN server made with [Wireguard Portal](https://wgportal.org/latest/). 
It provides an efficient, secure and logless VPN service with a web interface for managing users and peers, using [the Wireguard protocol](https://www.wireguard.com) as the underlying VPN technology.

This repository is a pretty small [Ansible playbook](https://www.redhat.com/en/ansible-collaborative) that deploys Wireguard Portal to any number of [Ubuntu](https://http://ubuntu.com) machines through [Docker](https://www.docker.com). 

## Deploying Genesis

Deployment is quite simple: clone the repository, install Ansible, configure the inventory, then run the playbook:

```bash
git clone https://github.com/Jack-Gledhill/genesis
pip install -r requirements.txt
# Edit the inventory file to add your hosts
ansible-playbook install.yml
```

## Connecting to Genesis

Genesis has two access points: a web interface, and the Wireguard server. 
The web interface is available at [`https://genesis.jackgledhill.com`](https://genesis.jackgledhill.com). 
It's proxied and secured by [Cloudflare](https://cloudflare.com), which is why the Wireguard server has to be accessed through a different subdomain: `connect.genesis.jackgledhill.com:51820`. 

## Can I get an account?

Probably not. 

## Mailing

Genesis has been configured to send emails through [smtp2go](https://smtp2go.com). 
Emails will be sent from `noreply@jackgledhill.com`. 