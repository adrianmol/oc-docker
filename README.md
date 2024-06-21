# OpenCart Docker

This repository should make it super simple to run [Opencart](http://www.opencart.com/) in docker containers.

## Installation
1. Firstly, create a project folder and place the OpenCart files inside there.
2. Add the oc-docker files:
- if you are using Git already you could add it as a submodule:

        $ git submodule add https://github.com/DockerIt/opencart-docker.git
- if not, either copy the files or clone into the project directory:

        $ git clone https://github.com/DockerIt/opencart-docker.git
3. It should look a bit like this:

        |-- project-root
        |   |-- database
        |   |-- docker
        |   |-- src
        |   |   |-- admin
        |   |   |-- catalog
        |   |   |-- image
        |   |   |-- etc...

4. Now, in the opencart-docker folder, we want run it and serve Opencart. The simplest way is:

        $ docker-compose up -d

5. Finally, we need to be able to access the site. We need to put the docker ip address into the HOSTS file.
   This will be different on different operating systems.
### Hosts
1. Simple. Docker is native so open `/etc/hosts` and add

        127.0.0.1 opencart.test

7. Visit http://opencart.test/ :-)

8. The OpenCart install is now really simple.

3. Click continue and then OpenCart should install, and you should be able to access your store! 