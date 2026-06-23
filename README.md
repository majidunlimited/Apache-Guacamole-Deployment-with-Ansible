# guacamole-1.5.5 using ansible and Nexus repository
This playbook can use for install Apache guacamole 1.5.5 with Nexus repository.
To download packages from Nexus repository, first you need to install Nexus. I use Sonatype Nexus Repository.
Every repositories on nexus has a URL. I create apt-hosted, apt-proxy and pypi-proxy repository.
If you dont have nexus repository, you can comment all the lines related to nexus.

# Nexus on source list
If you use this playbook, beaware that in target server, you will lost your source.list default repo of ubuntu. 
If you wanna use your nexus beside your default ubuntu repos, change /etc/apt/source.list path to /etc/apt/source.list.d/nexus.list.

# Version list
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
