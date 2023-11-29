# Web Server Project Overview

Throughout this project, I gained insights into the functioning of web servers and initiated practical usage. ALX provided a personal server, and I learned file transfer techniques using `scp` and Fabric, ultimately configuring the server with Nginx.

The server is accessible via [bdbnb.site](http://bdbnb.site).

## Project Tasks

### Task 0: Transfer a File to Your Server
- [0-transfer_file](./0-transfer_file): A Bash script facilitating the transfer of a file from Holberton's client to a server.
- Accepts four arguments: file path, server IP, `scp` username, and the path to the SSH private key.
- Utilizes `scp` to transfer the file to the user's home directory `~/`.

### Task 1: Install Nginx Web Server
- [1-install_nginx_web_server](./1-install_nginx_web_server): A Bash script configuring a new Ubuntu machine with Nginx.
- Nginx listens on port 80.
- A `curl` GET request to Nginx's root `/` returns a page containing the string `Hello World`.

### Task 2: Setup a Domain Name
- [2-setup_a_domain_name](./2-setup_a_domain_name): A text file documenting the domain name set up for the server through Gandi.

### Task 3: Redirection
- [3-redirection](./3-redirection): A Bash script configuring a new Ubuntu machine with Nginx.
- Similar setup to [1-install_nginx_web_server](./1-install_nginx_web_server).
- Additionally, the location `/redirect_me` implements a `301 Moved Permanently` redirection to another page.

### Task 4: Not Found Page 404
- [4-not_found_page_404](./4-not_found_page_404): A Bash script configuring a new Ubuntu machine with Nginx.
- Setup mirrors [1-install_nginx_web_server](./1-install_nginx_web_server).
- Includes a custom 404 page containing the string `Ceci n'est pas une page`.

### Task 5: Design a Beautiful 404 Page
- A custom-designed 404 error page for the server, accessible at [bdbnb.site/404](http://bdbnb.site/404).

### Task 6: Deploy Fast, Deploy Well
- [fabfile.py](./fabfile.py): A Python Fabric configuration file defining the following functions:
  - `pack`: Usage - `fabric pack`
    - Creates a tar gzipped archive named `holbertonwebapp.tar.gz` in the local directory.
  - `deploy`: Usage - `fabric -H <remote server IP> deploy`
    - Uploads `holbertonwebapp.tar.gz` to the `/tmp` directory of the remote server.
    - Creates the directory `/tmp/holbertonwebapp` on the remote server.
    - Untars `holbertonwebapp.tar.gz` in the `/tmp/holbertonwebapp` directory on the remote server.
  - `clean`: Deletes the archive `holbertonwebapp.tar.gz` in the local directory.