# Apache Guacamole Deployment with Ansible and Nexus OSS Repository
Automated deployment of Apache Guacamole 1.5.5 using Ansible and Nexus OSS Repository.

This project supports both online and offline installations by integrating with Sonatype Nexus Repository, making it suitable for enterprise environments with restricted Internet access. Make sure your Nexus server have access to Internet.

## Why I build this project?
Many enterprise environments don't have direct Internet access.

Installing Apache Guacamole manually in these environments will have some issues.

So this project automates the complete deployment process using Ansible while retrieving packages from an internal Nexus Repository.

## Features

- Automated Guacamole 1.5.5 installation.
- Offline package installation using Nexus proxy or hosted repository
- Apache Tomcat 9.0.118 deployment (Latest version for now)
- Dependency installation
- CVE fixes (Added for solving security issues)

# Nexus on source list
If you use this playbook, beaware that in target server, you will lost your source.list default repo of ubuntu. 
If you wanna use your nexus beside your default ubuntu repos, change /etc/apt/source.list path to /etc/apt/source.list.d/nexus.list.

# Technologies
 * Ubuntu 22.04 TLS (Jammy)
 * Tomcat 9 (latest version)
 * Guacamole 1.5.5
 * Ansible 2.17.11
 * Python 3.10

# Release 2.0.1 Published
Solve two CVE:
* CVE-2024-56337
* CVE-2026-31431

Go to releases.

## Future Improvements
- Will support Ubuntu 24.04
- Add Molecule tests
- Support Podman

## Lessons Learned

During this project I learned:

- Managing offline repositories
- Automating enterprise deployments
- Handling package dependencies
- Building reusable Ansible roles

## Real-world Use Case
This project was created for enterprise environments where Internet access is restricted.

Instead of downloading packages directly from public repositories, all dependencies are retrieved from an internal Sonatype Nexus Repository.
