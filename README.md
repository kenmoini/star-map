# star-map

## What is Star Map?

Star Map is a front-end for [Nebula](https://github.com/slackhq/nebula) bundled with the different services required to operate it at scale, such as Keycloak SSO, DNS, and more.

This is currently still a work-in-progress.

## Requirements

- Two publicly accessible nodes, a set of 2GB DigitalOcean Droplets would do
- A set of FQDNs serving pointing to the nodes:
  - sso.example.com to node1
  - star-map.example.com to node2
  - dns-{1,2}.example.com to node{1,2}

## Deployment

### Keycloak SSO

To deploy Keycloak SSO:

1. Clone down this repo and enter the `keycloak` directory
2. Modify the `vars/main.yaml` file to suit your infrastructure and needs
3. Modify the `inventory` file to point to your SSO server, node1, and set the username/SSH key location host variables
4. Run `ansible-playbook -i inventory deployer.yaml`
5. ??????
6. PROFIT!!!1

***A templated Realm and Roles/Groups import file(s) still need to be made to make (re)deployment even easier...***