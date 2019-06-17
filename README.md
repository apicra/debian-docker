# debian-docker
Install docker on debian


First, update your existing list of packages:

    sudo apt update

Next, install a few prerequisite packages which let apt use packages over HTTPS:

    sudo apt install apt-transport-https ca-certificates curl gnupg2 software-properties-common

Then add the GPG key for the official Docker repository to your system:

    curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -

Add the Docker repository to APT sources:

    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"

Next, update the package database with the Docker packages from the newly added repo:

    sudo apt update

#Make sure you are about to install from the Docker repo instead of the default Debian repo:

    apt-cache policy docker-ce
