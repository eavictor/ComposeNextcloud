Nextcloud running on Docker
===========================
Change username and password in ``nextcloud.yml`` before execute the command.

Installation
------------
1. Clone from GitHub

.. code-block::

    cd /home
    sudo git clone https://github.com/eavictor/ComposeNextcloud.git
    cd ComposeNextcloud
    mkdir mariadb
    mkdir data

2. Install Docker

.. code-block::

    sudo bash 1_install_docker.sh

3. Edit ``nextcloud.yml``

.. code-block::

    sudo nano nextcloud.yml

4. Start services (MariaDB, Redis, Nextcloud)

.. code-block::

    docker-compose -f nextcloud.yml up -d