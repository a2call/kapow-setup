# Kapow! Setup
The setup script for the Kapow! boilerplate for bespoke WordPress site development. 

## Requirements

You will need the following installed on your system before attempting to set-up a Kapow! project using this guide.

- [VirtualBox](http://www.virtualbox.org/), [Parallels](http://www.parallels.com) or another virtual machine
- [Vagrant](https://www.vagrantup.com/)
- [VVV a.k.a Varying Vagrant Vagrants](https://github.com/Varying-Vagrant-Vagrants/VVV)
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [NodeJS](https://nodejs.org/)
- [Bower](http://bower.io/#install-bower)
- [Grunt](http://gruntjs.com/installing-grunt)

It is also recommended that you are running WP CLI version `0.24.x` or greater to avoid a fatal error when running the `wp core install...` command which prevents the core WP tables from being added to the database. Run `wp cli update` to upgrade to the latest stable release.

## Installation

1) Create a new folder in your Vagrant web root e.g. `Vagrant/www/my-project`.

2) Download the `kapow.sh` script from this repo and move it to the folder you just created or grab it directly via the terminal using the commands below and:

`curl -O https://raw.githubusercontent.com/mkdo/kapow-setup/master/kapow-setup/kapow.sh`

`wget https://raw.githubusercontent.com/mkdo/kapow-setup/master/kapow-setup/kapow.sh`

3) Make the script executable via the command line using `chmod a+x kapow.sh`.

4) Run the script with `./kapow.sh` and up to five additional parameters to facilitate string replacement across the entire new Kapow! project you've created. 

*TIP: Create an alias called `getkapow` on your machine that invokes one of the above commands to fetch Kapow! before making it executable. Useful if you use Kapow! as much as we do!*

**Kapow! Setup Parameters**

The parameters must be added in the following order:

- Project Slug e.g. `avengers-initiative` *
- Project Nice Name e.g `"Avengers Initiative"`
- Author Name e.g. `"Director Fury"`
- Author Email e.g. `director@avengers.com`
- Author Website e.g. `www.avengers.com`

*NB: The project slug will be used for the theme folder name, theme textdomain, code namespace and database name.*

An example using all of the above would look like this:

`./kapow.sh the-avengers "The Avengers" "Nick Fury" nick@fury.com www.avengers.com`

*NB: Strings containing spaces must be encapsulated in double quotes.*
