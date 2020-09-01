# ansible-role-sc2-api-service

Ansible role for installing and launching [sc2-api-service](https://github.com/sc2pte/sc2-api-service) instance on Debian-based server.

Requires Nginx, Redis, Node.js, pm2 and [bnet-auth-service](https://github.com/sc2pte/bnet-auth-service) installed on the server. It *does not* install them automatically.

It builds the app from Git repository and generates backup of the previous deployment if available.

## Variables

| Variable name | Sample value | Description |
|-  |-  |-
| `sas_deploy_directory` | `/home/deploy/sc2-api-service` | Directory used to deploy project |
| `sas_backup_directory` | `/home/deploy/backups/sc2-api-service` | Directory used to generate backups of previous deployments as tgz files |

For project-specific environment variables, see [tasks/install.yml](https://github.com/sc2pte/ansible-role-sc2-api-service/blob/master/tasks/install.yml#L26).
