                    WordPress packaged by Bitnami 5.9.3-0
                  ==============================


1. OVERVIEW

The Bitnami Project was created to help spread the adoption of freely available, 
high quality, open source web applications. Bitnami aims to make it easier than 
ever to discover, download and install open source software such as document and 
content management systems, wikis and blogging software.

You can learn more about Bitnami at https://bitnami.com

WordPress is the world's most popular blogging and content management platform. 
Powerful yet simple, everyone from students to global corporations use it to 
build beautiful, functional websites.

You can learn more about WordPress at http://www.wordpress.org

The WordPress packaged by Bitnami is an installer that greatly simplifies the
installation of WordPress and runtime dependencies. It includes ready-to-run
versions of Apache, MariaDB and PHP.

WordPress packaged by Bitnami is distributed for free under the Apache 2.0 
license. Please see the appendix for the specific licenses of all open source 
components included.

You can learn more about Bitnami Stacks at https://bitnami.com/stacks/

2. FEATURES

- Easy to Install

Bitnami Stacks are built with one goal in mind: to make it as easy as
possible to install software. Our installers completely automate
the process of installing and configuring all of the software included in
each Stack, so you can have everything up and running in just a few clicks.

- Independent

Bitnami Stacks are completely self-contained, and therefore do not interfere
with any software already installed on your system. For example, you can
upgrade your system's MariaDB or Apache without fear of 'breaking' your
Bitnami Stack.

- Integrated

By the time you click the 'finish' button on the installer, the whole stack
will be integrated, configured and ready to go.

- Relocatable

Bitnami Stacks can be installed in any directory. This allows you to have
multiple instances of the same stack, without them interfering with each other.

3. COMPONENTS

WordPress packaged by Bitnami ships with the following software versions:

  - WordPress 5.9.3
  - WP-CLI 2.6.0
  - Apache 2.4.53
  - Varnish(TM) (Only supported on Linux and OS X)
  - MariaDB 10.4.24
  - PHP 8.0.17
  - phpMyAdmin 5.1.3

4. REQUIREMENTS

To install WordPress packaged by Bitnami you will need:

    - Intel x86 or compatible processor
    - Minimum of 700 MB RAM
    - Minimum of 150 MB hard drive space
    - TCP/IP protocol support
    - Compatible operating systems:
      - An x86 or x64 Linux operating system.
      - A Windows operating system such as Windows Vista, Windows 7, Windows 8, Windows 10, Windows Server 2008 or Windows Server 2012.
			- An OS X operating system.

5. INSTALLATION

The WordPress packaged by Bitnami is distributed as a binary executable installer.
It can be downloaded from:

https://bitnami.com/stacks/

The downloaded file will be named something similar to:

bitnami-wordpress-5.9.3-0-linux-x64-installer.run on Linux 64 bit or
bitnami-wordpress-5.9.3-0-windows-installer.exe on Windows or
bitnami-wordpress-5.9.3-0-osx-x64-installer.dmg on OS X.

On Linux, you will need to give it executable permissions:

chmod 755 bitnami-wordpress-5.9.3-0-linux-x64-installer.run


To begin the installation process, double-click on that file, and you will
be greeted by the 'Welcome' screen. Pressing 'Next' will take you to the
Component Selection screen, where you can select the phpMyAdmin component. This
tool intended to handle the administration of MariaDB over the web.

The next screen is the Installation Folder, where you can select where Bitnami
stack will be installed. If the destination directory does not exist, it will
be created as part of the installation.

The next screen will prompt you for data necessary to create the initial
admin user:

Username and password: You will use this information to log-in into the
administrative interface. The password you provide here will also be used to
protect other parts of the installation. Please see the section named
"Usernames and Passwords" later in this document.

Real name: The name that will be displayed in the application.

Email address: Your email address.

The next screen will vary, depending on whether the ports needed by the
bundled Apache and MariaDB are already taken. The default listening port for
Apache is 8080 on Linux or port 80 on Windows and for MariaDB is 3006. If those
ports are already in use by other applications, you will be prompted for
alternate ports to use.

The next screen will allow you to configure the final details of your
WordPress installation:

Blog name: Title of your blog, which will be displayed to visitors

Hostname: The hostname for your blog, such as www.example.com. This
information will be used by WordPress when creating certain links.

Once the information has been entered, the installation will proceed to copy
the files to the target installation directory and configure the different
components. One this process has  been completed, you will see the
'Installation Finished' page. You can choose to launch WordPress packaged by Bitnami
at this point. If you do so, your default web browser will open and
display the Welcome page for the WordPress packaged by Bitnami.

If you received an error message during installation, please refer to
the Troubleshooting section.

The rest of this guide assumes that you installed Bitnami WordPress Stack
in /home/user/wordpress-5.9.3-0 on Linux or
C:\Bitnami\wordpress-5.9.3-0 on Windows or
/Applications/wordpress-5.9.3-0 on OS X and that you use port 8080
for Apache on Linux or port 80 on Windows and 3306 for MariaDB.

6. STARTING AND STOPPING WORDPRESS PACKAGED BY BITNAMI

The Bitnami Application Manager is a simple graphical interface included in
the stacks that can start and stop the Bitnami servers. It is are located
in the same installation directory.

To start the utility, double click the file named ‘manager-linux’,
'manager-windows' or 'manager-osx' from your file browser.

Alternatively, you can also start and stop the services manually, as explained below.

To start/stop/restart application on Linux and OSX you can use the included ctlscript.sh
utility, as shown below:

       ./ctlscript.sh (start|stop|restart)
       ./ctlscript.sh (start|stop|restart) mariadb
       ./ctlscript.sh (start|stop|restart) apache
       ./ctlscript.sh (start|stop|restart) varnish

  start      - start the service(s)
  stop       - stop  the service(s)
  restart    - restart or start the service(s)

On Windows, you can start and stop WordPress packaged by Bitnami using the shortcuts created
in the Start Menu, under Programs -> Bitnami -> Bitnami Service

That will start Apache service. Once started, you can open your
browser and access the following URL on Linux or OS X:

http://127.0.0.1:8080/wordpress/

And you can access the following URL on Windows:

http://127.0.0.1/wordpress/

If you selected an alternate port during installation, for example 18080, the
URL will look like:

http://127.0.0.1:18080/wordpress/

If you are accessing the machine remotely, you will need to replace
127.0.0.1 with the appropriate IP address or hostname.

7. DIRECTORY STRUCTURE

The installation process will create several subfolders under the main
installation directory:

	apache2/: Apache Web server.
        varnish/: Varnish(TM) Cache
	php/: PHP Scripting Language.
	mariadb/: MariaDB Database.
	apps/
	  wordpress/: WordPress application folder
	    conf/: WordPress Apache configuration files
	    htdocs/: WordPress PHP application files
	  phpMyAdmin/: phpMyAdmin application folder (optional)

8. DEFAULT USERNAMES AND PASSWORDS

The WordPress administrative user and password are the ones you set at
installation time.

MariaDB admin user is called 'root', and its password is the same as the
WordPress administrative user password.

The default MariaDB non-root account used to access the bitnami_wordpress database
is named bn_wordpress, and its password is random.

The phpMyAdmin administrative user is 'root'.

9. TROUBLESHOOTING

You can find more information about this product at:

https://docs.bitnami.com/

We also encourage you to post your questions and suggestions at:

https://community.bitnami.com

We also encourage you to sign up for our newsletter, which we'll use to
announce new releases and new stacks. To do so, just register at:
https://bitnami.com/newsletter.

9.1 Installer

# Installer Payload Error

If you get the following error while trying to run the installer from the
command line:

"Installer payload initialization failed. This is likely due to an
incomplete or corrupt downloaded file"

The installer binary is not complete, likely because the file was
not downloaded correctly. You will need to download the file and
repeat the installation process.

9.2 Apache

If you find any problem starting Apache, the first place you should check is
the Apache error log file:

/home/user/wordpress-5.9.3-0/apache2/logs/error.log on Linux or
C:\bitnami\wordpress-5.9.3-0\apache2\logs\error.log on Windows or
/Applications/wordpress-5.9.3-0/apache2/logs/error.log.

Most errors are related to not being able to listen to the default port.
Make sure there are no other server programs listening at the same port
before trying to start Apache. Some programs, such as Skype, may also use
port 80. For issues not covered in this Quick Start guide, please refer to
the Apache documentation, which is located at http://httpd.apache.org/docs/

9.3 MariaDB

The following are some common problems:

# Access denied when trying to connect to MariaDB.

If you get an Access Denied message while trying to connect to
MariaDB, make sure you are using the correct username and password.

# "Can't connect to server" message.

Make sure that the MariaDB daemon is up and running. Remember also that if
during installation you selected a different listening port for MariaDB, you
may need to pass that as an extra command line option.

For help in troubleshooting MariaDB errors, you may want to reference the
the MariaDB manual, which you will find at https://mariadb.com/kb/en/documentation/

9.4 Varnish(TM)

# Changing Varnish(TM) port

The installer will automatically set for the Varnish(TM) port the first one free after
the Apache port. This works fine to test it but if you want to use Varnish(TM) in a
production environment, you will  probably want to change its port to a more
appropriate one (for example, 80 instead of 81) and change Apache port if it is
currently taking it.

You can find a guide of how to do this in the below link:

https://docs.bitnami.com/general/apps/wordpress/administration/configure-use-varnish/

# Configuring Varnish(TM) to use a WordPress-specific configuration file

By default, Varnish(TM) uses the default configuration settings. To make WordPress
properly handle when the cache must be refreshed or ignored, that configuration
file must be replaced. The below article explains how to configure Varnish(TM)
with WordPress:

https://docs.bitnami.com/general/apps/wordpress/administration/configure-use-varnish/

9.5 WordPress

For any problem related to WordPress, please visit
http://codex.wordpress.org/Troubleshooting


10. LICENSES

Apache Web Server is distributed under the Apache License v2.0, which
is located at http://www.apache.org/licenses/LICENSE-2.0

Varnish(TM) cache is distributed under the BSD License, located at
http://www.opensource.org/licenses/bsd-license.php

MariaDB is distributed under the GNU General Public License v2, which is
located at http://www.gnu.org/licenses/old-licenses/gpl-2.0.html

PHP and related libraries are distributed under the PHP License v3.01,
which is located at http://www.php.net/license/3_01.txt

WordPress is distributed under the GNU General Public License v2,
which is located at
http://www.gnu.org/licenses/old-licenses/gpl-2.0.html

curl is distributed under the Curl License, which is located at
http://curl.haxx.se/docs/copyright.html

expat is distributed under the MIT License, which is located at
http://www.jclark.com/xml/copying.txt

gd is distributed under the gd License, which is located at
http://www.boutell.com/gd/manual2.0.33.html

IMAP is distributed under the University of Washington Free-Fork
License, located at http://www.washington.edu/imap/legal.html

jpegsrc is distributed under The Independent JPEG Group's JPEG
software license, which is located at
http://dev.w3.org/cvsweb/Amaya/libjpeg/README?rev=1.2

libiconv is distributed under the Lesser General Public License
(LGPL), located at http://www.gnu.org/copyleft/lesser.html

Freetype is released under The Freetype Project License, that is located at
http://freetype.sourceforge.net/FTL.TXT
