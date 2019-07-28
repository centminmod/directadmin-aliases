# DirectAdmin SSH Command Aliases

Idea originally came from my [DirectAdmin forum thread](https://forum.directadmin.com/showthread.php?t=58333), so thought it would be best to put the info into a Github repo so folks can contribute to the list via pull requests adding to the [`contributions`](https://github.com/centminmod/directadmin-aliases/contributions) subfolder with a new markdown `.md` file with your name. Example my contributions are at [here](https://github.com/centminmod/directadmin-aliases/blob/master/contributions/george.liu.md).

## SSH Command Aliases' Purpose

To save time typing I usually setup my own alias command shortcuts in /root/.bashrc to allow me to navigate a system more quickly. I am sure seasoned DirectAdmin pros do the same.

For addition to `/root/.bashrc`

```
daconf='/usr/local/directadmin/conf/directadmin.conf'
cbconf='/usr/local/directadmin/custombuild/options.conf'
alias domainlogsdir='pushd /var/log/httpd/domains/'
alias directadmin='/usr/local/directadmin/directadmin'
alias dadir='pushd /usr/local/directadmin/'
alias dashdir='pushd /usr/local/directadmin/scripts'
alias cbdir='pushd /usr/local/directadmin/custombuild'
alias cb='/usr/local/directadmin/custombuild/build'
alias cbconfig='/usr/local/directadmin/custombuild/build used_configs'
alias cbopts='/usr/local/directadmin/custombuild/build options'
alias cbhelp='/usr/local/directadmin/custombuild/build opt_help full'
alias cbvers='/usr/local/directadmin/custombuild/build versions'
alias mysqladmin='mysqladmin --defaults-extra-file=/usr/local/directadmin/conf/my.cnf'
alias mysqldump='mysqldump --defaults-extra-file=/usr/local/directadmin/conf/my.cnf'
alias mysql='mysql --defaults-extra-file=/usr/local/directadmin/conf/my.cnf'
```

## Examples

```
directadmin o
Compiled on 'CentOS 7.0 64-Bit'
Compile time: Jul 12 2019 at 09:37:52
Timestamp: '1562945823'
Compiled with IPv6
```

```
cbconfig
Apache configuration file: /usr/local/directadmin/custombuild/configure/ap2/configure.apache
PHP (default) php.ini file: /usr/local/php73/lib/php.ini
PHP (additional) php.ini file: /usr/local/php72/lib/php.ini
PHP (additional, 3rd) php.ini file: /usr/local/php56/lib/php.ini
PHP (default) configuration file: /usr/local/directadmin/custombuild/configure/fpm/configure.php73
PHP (additional) configuration file: /usr/local/directadmin/custombuild/configure/fpm/configure.php72
PHP (additional, 3rd) configuration file: /usr/local/directadmin/custombuild/configure/fpm/configure.php56
PureFTPD configuration file: /usr/local/directadmin/custombuild/configure/pureftpd/configure.pureftpd
Exim Makefile: http://files2.directadmin.com/services/custombuild/Makefile
Dovecot configuration file: /usr/local/directadmin/custombuild/configure/dovecot/configure.dovecot
```

```
cb versions | grep PHP
Latest version of PHP 5.6: 5.6.40
Installed version of PHP 5.6: 5.6.40
Latest version of PHP 7.2: 7.2.20
Installed version of PHP 7.2: 7.2.20
Latest version of PHP 7.3: 7.3.7
Installed version of PHP 7.3: 7.3.7
```
