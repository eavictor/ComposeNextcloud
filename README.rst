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

    Note: <username> is for adding user into docker group, don't forget to pass username in

.. code-block::

    sudo bash 1_install_docker.sh <username>

3. Edit ``nextcloud.yml``

.. code-block::

    sudo nano nextcloud.yml

4. Start services (MariaDB, Redis, Nextcloud)

.. code-block::

    docker-compose -f nextcloud.yml up -d