# OVA for PHP Application Development and Testing with CodeIgniter 3.1.13

This OVA is configured to facilitate the development and testing of PHP applications based on the CodeIgniter 3.1.13 framework in local environments. The configuration is designed to be used in a development environment and does not include VHOSTs, IPTables, or SSL configurations to avoid unnecessary complications in this context.

## OVA Features

- **Operating System:** Ubuntu 24.04 LTS
- **Web Server:** Apache 2.4.62
- **Programming Language:** PHP 8.3
- **Framework:** CodeIgniter 3.1.13
- **Database:** MySQL 8.3.9
- **Session, SSH, and MySQL Access:**
  - **User:** `devadmin`
  - **Password:** `d3v4dm1n`

## Download, Access, and Use

First, it is necessary to download the OVA. To do this, click on the following link:
[Application Development with CI 3.1.13.ova](https://mega.nz/file/5oJCEYja#M6ICl_uhYz6b5lHPucNpQq7NyWLixTW-Eh0pOLeUcxI)

To use this OVA, you need to import it into Virtualbox or VMware and configure the network interface as NAT or another option. Once the VM is configured and started, you should access it with the Session credentials, and to obtain the machine's IP address, run the command

```bash
ip a
```

### SSH

To access the virtual machine via SSH, use the following credentials:

- **User:** `devadmin`
- **Password:** `d3v4dm1n`

```bash
ssh devadmin@<OVA-IP>
```

### MySQL

To access MySQL:

```bash
mysql -u devadmin -p
```

### Working Environment

The working environment is located in the `/var/www/html` directory, which is divided into:

- `/var/www/html/sql`: for the database manager (PHPMyAdmin 5.2.1), accessible via the URL: http://<OVA-IP>/sql/
- `/var/www/html/public`: for CodeIgniter 3.1.13, accessible via the URL: http://<OVA-IP>/public/

### Apache

Apache is configured to serve the project from the `/var/www/html` directory. It is not necessary to modify VHOST configurations for the development environment.

### PHP

The OVA includes PHP 8.3 with the necessary extensions to run CodeIgniter and other common web applications. If you need to install additional extensions, you can do so using `apt`.

```bash
sudo apt install php-<extension>
```

## Additional Notes

- This OVA is configured for local environments and is not recommended for production use.
- For any problems or questions, contact me.

## License

This OVA is provided as-is, without any warranties. Use at your own risk.
