# Ansible-HTPC
A quick and dirty github project to get a Ubuntu 18.04 LTS VM up and running with docker containers for:
- Sonarr
- Radarr
- Deluge
- NzbGet
- Jackett
- Plex

## Getting Started
The following steps should get you to the point where your already deployed VM will have all the above containers running on.

### Prerequisites
- Ubuntu 18.04 LTS with SSH Access

### Installation
- Ensure you change the values in host_servers.yml to your local paths where you want things to be, timezone, etc.
- Ensure you add your IP or Hostname to inventories/hosts
`ansible-playbook -i inventories/hosts playbook.yml -u <remote user>`

## Using
You should now have the following services running with your respective IP/Hostname:
- [Sonarr](http://IP:8989)
- [Radarr](http://IP:7878)
- [Deluge](http://IP:8112)
- [Nzbget](http://IP:6789)
- [Jackett](http://IP:9117)

### TODO
- Add letsencrypt container and modifications to work with default containers
- Other things...