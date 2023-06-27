# Ansible Project
[![Ansible](https://img.shields.io/badge/Ansible-red)](https://www.ansible.com/)

This Ansible repo contains a collection of roles and playbooks for automating the configuration and management of Linux hosts. It provides a streamlined approach for deploying and managing various components such as Docker, PostgreSQL, Prometheus, and a web server using Ansible. More roles and playbooks will be added.

## Features

- Organizing directory structure for roles and playbooks.
- Easy customization of role variables to adapt to different environments.
- Modular playbook structure for orchestrating multiple roles.

## Repository Structure
The repository follows a standard structure to keep the Ansible code organized and maintainable:

- `ansible.cfg`: Ansible configuration file.
- `inventories/`: Directory for inventory-related files.
- `playbooks/`: Directory for playbooks.
- `roles/`: Directory containing individual roles.
- `docker/`: Role for installing and configuring Docker.
- `postgresql/`: Role for installing and configuring PostgreSQL.
- `prometheus/`: Role for installing and configuring Prometheus.
- `webserver/`: Role for installing and configuring a web server.

## Usage
1. Clone the repo to your local machine. `git clone https://github.com/samanxsy/ansible-repo.git`
2. Modify the inventory file (`inventories/hosts`) to specify the hosts you want to target.
3. Customize role variables as per your requirements in the respective role's `defaults/main.yml`.
4. Run the main playbook (`playbooks/main.yml`) to execute the desired roles and configure the hosts, or run the roles separately
```
ansible-playbook playbooks/main.yml -i inventories/hosts
```
- To run a specific role, e.g webserver
```
ansible-playbook playbooks/main.yml -i inventories/hosts --tags webserver
```

## Contributing

Contributions are welcome! If you have any suggestions, improvements, or a new role to add, please feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
