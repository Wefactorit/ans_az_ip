# Ansible Role: Public IP Azure
This Ansible project aims to meet the demand for the creation of public IP addresses.


## Overview
----------------------------------
This role create a public ip in AZURE , if you need more information about public ip in AZURE [here](https://docs.microsoft.com/fr-fr/azure/virtual-network/virtual-network-ip-addresses-overview-arm).


## Requirements component
----------------------------------
- Ansible 2.8.4
- AZ cli 2.0.52
- Azure 2.0.0
- python 2.7

## Requirements Azure Infrastructure
You already need to have an Azure resource group
See this playbook for creating a group resource: [WefactoryRG](https://github.com/Wefactorit/ans_az_resource_group)

## Installation
---------------------------------

```
ansible-galaxy install Wefactoritans_az_ip
```

## Role Variables
Available variables are listed below, along with default values (see defaults/main.yml):

#### GENERAL

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| project | Name of the project used for the resources_pattern | string | - | yes
| env | Environment's name, int, pprod, prod, qual, dev...| string | - | yes
| location_short | short name of your location for the resources_pattern | string | - | yes |
| resources_pattern | writing charter | string |  "{{ project }}-{{ env }}-{{ location_short }}" | yes |
| resource_group_name | know in which group resource to put an ip address | string | - | yes |
| type | The type of the DNS zone private or public| string | - | yes |
| public_ip_address_name | name of th public ip  | string | - | yes |
| public_ip_address_allocation_method | Method allocation of IP | string | Dynamic | yes |
| public_ip_address_domain_name | domain name of public ip addres | string | - | yes |

## Author
----------------------------------
- Saba DevOps.

## Acknowlegement
----------------------------------
Thank Wefactorit Team.
