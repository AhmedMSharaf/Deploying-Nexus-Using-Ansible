# Deploying-Nexus-Using-Ansible
Project Documentation
This Ansible playbook automates the installation and configuration of the Nexus Repository Manager on a remote target server.

### Prerequisites
- Ansible must be installed on the local machine that will run the playbook.
- The target server must have SSH connectivity configured and the SSH credentials must be accessible to the local machine.
- The target server must have the Yum package manager installed and configured.
### Playbook Tasks
- Update the Yum packages to their latest version.
- Install the wget package.
- Install the Java 1.8.0 OpenJDK package.
- Create the /app directory if it does not exist.
- Change working directory to /app.
- Download the latest Nexus tarball from the Sonatype website.
- Extract the Nexus archive to the /app directory.
- Rename the Nexus directory to /app/nexus.
- Add a new user named nexus.
- Change ownership of the /app/nexus directory to nexus.
- Change ownership of the /app/sonatype-work directory to nexus.
- Open and configure the nexus.rc file.
- Create the Nexus systemd unit file /etc/systemd/system/nexus.service.
- Add the Nexus service to boot using the chkconfig command.
- Start the Nexus service.
## How to Run the Playbook
- Open a terminal on the local machine.
- Navigate to the directory containing the playbook.
- Run the playbook using the following command:
"ansible-playbook playbook-nexus.yaml -i inventory"
