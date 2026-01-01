# Architecture du laboratoire Wazuh sur AWS

## Composants
- EC2-1 : Wazuh All-in-One (Ubuntu 22.04)
- EC2-2 : Client Linux (Ubuntu 22.04)
- EC2-3 : Client Windows Server

## Flux réseau
- Agents → Wazuh Manager : TCP 1514
- Enrôlement agents : TCP 1515
- Accès Dashboard : HTTPS 443 (ou 5601 selon configuration)

## Réseau
- Toutes les instances sont dans le même VPC et subnet
- Communication limitée via Security Groups
