# DirectAdmin SSH Command Aliases

Idea originally came from my [DirectAdmin forum thread](https://forum.directadmin.com/showthread.php?t=58333), so thought it would be best to put the info into a Github repo so folks can contribute to the list via pull requests adding to the [`contributions`](https://github.com/centminmod/directadmin-aliases/tree/master/contributions) subfolder with a new markdown `.md` file with your name. Example my contributions are at [here](https://github.com/centminmod/directadmin-aliases/blob/master/contributions/george.liu.md).

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
alias daupdate='cd /usr/local/directadmin/custombuild; time ./build update_versions'
alias cbdir='pushd /usr/local/directadmin/custombuild'
alias cb='/usr/local/directadmin/custombuild/build'
alias cbconfig='/usr/local/directadmin/custombuild/build used_configs'
alias cbopts='/usr/local/directadmin/custombuild/build options'
alias cbhelp='/usr/local/directadmin/custombuild/build opt_help full'
alias cbvers='/usr/local/directadmin/custombuild/build versions'
alias mysqladmin='mysqladmin --defaults-extra-file=/usr/local/directadmin/conf/my.cnf'
alias mysqldump='mysqldump --defaults-extra-file=/usr/local/directadmin/conf/my.cnf'
alias mysql='mysql --defaults-extra-file=/usr/local/directadmin/conf/my.cnf'
alias phpconfig='for pc in $(ls -1 /usr/local/php*/bin/php-config); do echo; $pc; done'
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

```
phpconfig

Usage: /usr/local/php56/bin/php-config [OPTION]
Options:
  --prefix            [/usr/local/php56]
  --includes          [-I/usr/local/php56/include/php -I/usr/local/php56/include/php/main -I/usr/local/php56/include/php/TSRM -I/usr/local/php56/include/php/Zend -I/usr/local/php56/include/php/ext -I/usr/local/php56/include/php/ext/date/lib]
  --ldflags           [ -L/usr/local/lib -L/usr/local/icu/lib]
  --libs              [-lcrypt   -lz -lexslt -lresolv -lcrypt -lrt -lmcrypt -lltdl -lstdc++ -liconv -lpng -lz -ljpeg -lcurl -lz -lpcre -lrt -lm -ldl -lnsl  -lsystemd -lxml2 -lz -liconv -lm -ldl -lgssapi_krb5 -lkrb5 -lk5crypto -lcom_err -lssl -lcrypto -lcurl -lxml2 -lz -liconv -lm -ldl -lssl -lcrypto -lfreetype -licui18n -licuuc -licudata -licuio -lxml2 -lz -liconv -lm -ldl -lxml2 -lz -liconv -lm -ldl -lcrypt -lxml2 -lz -liconv -lm -ldl -lxml2 -lz -liconv -lm -ldl -lxml2 -lz -liconv -lm -ldl -lxslt -lxml2 -lz -liconv -ldl -lm -lssl -lcrypto -lcrypt ]
  --extension-dir     [/usr/local/php56/lib/php/extensions/no-debug-non-zts-20131226]
  --include-dir       [/usr/local/php56/include/php]
  --man-dir           [/usr/local/php56/php/man]
  --php-binary        [/usr/local/php56/bin/php56]
  --php-sapis         [ cli fpm cgi]
  --configure-options [--prefix=/usr/local/php56 --program-suffix=56 --enable-fpm --with-fpm-systemd --with-config-file-scan-dir=/usr/local/php56/lib/php.conf.d --with-curl --with-gd --enable-gd-native-ttf --with-gettext --with-jpeg-dir=/usr/local/lib --with-freetype-dir=/usr/local/lib --with-libxml-dir=/usr/local/lib --with-kerberos --with-openssl --with-mcrypt --with-mhash --with-mysql=mysqlnd --with-mysql-sock=/var/lib/mysql/mysql.sock --with-mysqli=mysqlnd --with-pcre-regex=/usr/local --with-pdo-mysql=mysqlnd --with-pear --with-png-dir=/usr/local/lib --with-xsl --with-zlib --enable-zip --with-iconv=/usr/local --enable-bcmath --enable-calendar --enable-exif --enable-ftp --enable-sockets --enable-soap --enable-mbstring --with-icu-dir=/usr/local/icu --enable-intl CC=ccache CXX=ccache CXXFLAGS=-std=c++11 -DU_USING_ICU_NAMESPACE=1]
  --version           [5.6.40]
  --vernum            [50640]

Usage: /usr/local/php72/bin/php-config [OPTION]
Options:
  --prefix            [/usr/local/php72]
  --includes          [-I/usr/local/php72/include/php -I/usr/local/php72/include/php/main -I/usr/local/php72/include/php/TSRM -I/usr/local/php72/include/php/Zend -I/usr/local/php72/include/php/ext -I/usr/local/php72/include/php/ext/date/lib]
  --ldflags           [ -L/usr/local/lib -L/usr/local/icu/lib]
  --libs              [-lcrypt   -lz -lexslt -lresolv -lcrypt -lsodium -lrt -lstdc++ -liconv -lpng -lz -ljpeg -lwebp -lz -lpcre -lrt -lm -ldl -lnsl  -lsystemd -lxml2 -lz -liconv -lm -ldl -lgssapi_krb5 -lkrb5 -lk5crypto -lcom_err -lssl -lcrypto -lcurl -lxml2 -lz -liconv -lm -ldl -lssl -lcrypto -lfreetype -licui18n -licuuc -licudata -licuio -lxml2 -lz -liconv -lm -ldl -lxml2 -lz -liconv -lm -ldl -lcrypt -lxml2 -lz -liconv -lm -ldl -lxml2 -lz -liconv -lm -ldl -lxml2 -lz -liconv -lm -ldl -lxslt -lxml2 -lz -liconv -ldl -lm -lssl -lcrypto -lcrypt ]
  --extension-dir     [/usr/local/php72/lib/php/extensions/no-debug-non-zts-20170718]
  --include-dir       [/usr/local/php72/include/php]
  --man-dir           [/usr/local/php72/php/man]
  --php-binary        [/usr/local/php72/bin/php72]
  --php-sapis         [ cli fpm phpdbg cgi]
  --configure-options [--prefix=/usr/local/php72 --program-suffix=72 --enable-fpm --with-fpm-systemd --with-config-file-scan-dir=/usr/local/php72/lib/php.conf.d --with-curl --with-gd --with-gettext --with-jpeg-dir=/usr/local/lib --with-freetype-dir=/usr/local/lib --with-libxml-dir=/usr/local/lib --with-kerberos --with-openssl --with-mhash --with-mysql-sock=/var/lib/mysql/mysql.sock --with-mysqli=mysqlnd --with-pcre-regex=/usr/local --with-pdo-mysql=mysqlnd --with-pear --with-png-dir=/usr/local/lib --with-sodium=/usr/local --with-webp-dir=/usr/local/lib --with-xsl --with-zlib --enable-zip --with-iconv=/usr/local --enable-bcmath --enable-calendar --enable-exif --enable-ftp --enable-sockets --enable-soap --enable-mbstring --with-icu-dir=/usr/local/icu --enable-intl]
  --version           [7.2.20]
  --vernum            [70220]

Usage: /usr/local/php73/bin/php-config [OPTION]
Options:
  --prefix            [/usr/local/php73]
  --includes          [-I/usr/local/php73/include/php -I/usr/local/php73/include/php/main -I/usr/local/php73/include/php/TSRM -I/usr/local/php73/include/php/Zend -I/usr/local/php73/include/php/ext -I/usr/local/php73/include/php/ext/date/lib]
  --ldflags           [ -L/usr/local/lib -L/usr/local/icu/lib]
  --libs              [-lcrypt   -lz -lexslt -lresolv -lcrypt -lsodium -lrt -lstdc++ -liconv -lpng -lz -ljpeg -lwebp -lz -lrt -lm -ldl -lnsl  -lsystemd -lxml2 -lz -liconv -lm -ldl -lgssapi_krb5 -lkrb5 -lk5crypto -lcom_err -lssl -lcrypto -lpcre2-8 -lcurl -lxml2 -lz -liconv -lm -ldl -lssl -lcrypto -lfreetype -licui18n -licuuc -licudata -licuio -lxml2 -lz -liconv -lm -ldl -lxml2 -lz -liconv -lm -ldl -lcrypt -lxml2 -lz -liconv -lm -ldl -lxml2 -lz -liconv -lm -ldl -lxml2 -lz -liconv -lm -ldl -lxslt -lxml2 -lz -liconv -ldl -lm -lssl -lcrypto -lcrypt ]
  --extension-dir     [/usr/local/php73/lib/php/extensions/no-debug-non-zts-20180731]
  --include-dir       [/usr/local/php73/include/php]
  --man-dir           [/usr/local/php73/php/man]
  --php-binary        [/usr/local/php73/bin/php73]
  --php-sapis         [ cli fpm phpdbg cgi]
  --configure-options [--prefix=/usr/local/php73 --program-suffix=73 --enable-fpm --with-fpm-systemd --with-config-file-scan-dir=/usr/local/php73/lib/php.conf.d --with-curl --with-gd --with-gettext --with-jpeg-dir=/usr/local/lib --with-freetype-dir=/usr/local/lib --with-libxml-dir=/usr/local/lib --with-kerberos --with-openssl --with-mhash --with-mysql-sock=/var/lib/mysql/mysql.sock --with-mysqli=mysqlnd --with-pcre-regex=/usr/local --with-pdo-mysql=mysqlnd --with-pear --with-png-dir=/usr/local/lib --with-sodium=/usr/local --with-webp-dir=/usr/local/lib --with-xsl --with-zlib --enable-zip --without-libzip --with-iconv=/usr/local --enable-bcmath --enable-calendar --enable-exif --enable-ftp --enable-sockets --enable-soap --enable-mbstring --with-icu-dir=/usr/local/icu --enable-intl]
  --version           [7.3.7]
  --vernum            [70307]
```