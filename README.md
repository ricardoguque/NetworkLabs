# Network Labs

This repository contains the lab definitions, the variables for startup configs and the pipeline to deploy code uptade to my home server using Github Actions so the user can start the lab the want to choose.

## Technologies used

- [Docker](https://www.docker.com/)
- [Container Lab](https://containerlab.srlinux.dev/)
- [Github Actions](https://github.com/ricardoguque/NetworkLabs/actions/workflows/deploy.yml)
- [Arista cEOS](https://www.arista.com/en/products/eos/eos-virtual-machine)
- [Arista vEOS](https://www.arista.com/en/products/eos/eos-virtual-machine)
- [Mikrotik CHR](https://mikrotik.com/download)
- [YAML](https://yaml.org/)
- [Python](https://www.python.org/)
- [Jinja2](https://jinja.palletsprojects.com/en/3.0.x/)

## Labs

- [Spine and Leaf](/labs/closs_5L_4S_4SS.yml)

## How to use

The pipeline will ensure the host has the lates updates of the code and the labs. The user just need to go to `/home/richo/topos` and run the lab they want to use.

### Deploy a lab

```bash
cd /home/richo/topos
sudo containerlab --topo <topology>.yml deploy
```

### Inspect management information

```bash
sudo containerlab --topo <topology>.yml inspect
```

### Login to a container

```bash
sudo docker exec -it <container-name/id> bash
```

### Login via ssh to a device

```bash
ssh admin@<ip/container name from inspect>
```

Normally the password is `admin`

### Show topology

```bash
sudo containerlab --topo <topology>.yml graph
```

### Stop a lab

```bash
sudo containerlab --topo <topology>.yml destroy
```
