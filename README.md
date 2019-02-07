# LinuxServerConfig
### Project Overview
This a documentation for a baseline installation of a Linux server and prepare it to host the web applications. This will secure configured server from a number of attack vectors, install and configure a database server, and deploy existing applications

### Why this Project?
A deep understanding of exactly what the web applications are doing, how they are hosted, and the interactions between multiple systems are what define one as a Full Stack Web Developer. This demonstrate how to turn a brand-new, bare bones, Linux server into the secure and efficient web application host the existing applications need.


## Server Access Details:
IP = 54.79.116.131
URL = http://54.79.116.131/catalogue/

## Software summary:
   - Ubuntu 18.04 LTS on AWS LightSail\
   - Apache HTTP server \
   - PostgreSQL Database\
   - Python Packages for Flask Application\
   - Git\

## Configuration:
  - SSH mapped to port 2200 and installed access keys\
  - UFW firewall rules configuration\
  - Add and configured users for database and sudo access\
  - Postgresql installation and setup:\
      
      * To install use: \
         sudo apt-get install postgresql postgresql-contrib\
         
      * Setup accounts and prepare catalogue database:
         sudo adduser catalogue\
         sudo -u postgres createuser catalogue\
         psql> create database catalogue with owner catalogue;\
         psql> alter role catalogue PASSWORD='menu';\
         cd /var/www/html/catalogue\
         python db_set_schema.py\
         python db_insert_values.py\
 **[Back to top](#LinuxServerConfig)**
  
## References:
 Following references found to be usefule while setting up the server. Full credit to the authors
 https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-18-04
 https://medium.com/@esteininger/python-3-5-flask-apache2-mod-wsgi3-on-ubuntu-16-04-67894abf9f70

**[Back to top](#LinuxServerConfig)**

## Contributing
Open an issue first to discuss potential changes/additions.

**[Back to top](#LinuxServerConfig)**

## License

#### (The MIT License)

Copyright (c) 2019 Nirosh Gunaratne

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
        distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

        The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

        THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
        EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
        IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
        TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

**[Back to top](#LinuxServerConfig)**











      
