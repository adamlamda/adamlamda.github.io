# Setup the test framework

### Install composer globally
```sh
$ curl -sS https://getcomposer.org/installer | php
$ mv composer.phar /usr/local/bin/composer
```
You can read the official documentation [here](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx)
### Install Behat
To install behat and other dependencies run the following command on the project root: 
```sh
$ composer install
```
### Configure Behat
run the following command:
```sh
$ cp default.behat.yml behat.yml
```
Edit _behat.yml_ file and customize your **base_url**

### Initial setup
Create a database, but keep it empty

```sh
$ mysqladmin -uroot -p create phplisttestdb
$ mysqladmin -uroot -p -e "grant all on phplisttestdb.* to phplist@localhost identified by 'testpassword'"
```

edit your phplist config file to use these details

### Run The tests
Execute the following command:
```sh
$ vendor/bin/behat
```
### TODO
Add writing tests documentation.
