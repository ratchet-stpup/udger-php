# Udger client for PHP
Local parser is very fast and accurate useragent string detection solution. Enables developers to locally install and integrate a highly-scalable product.
We provide the detection of the devices (personal computer, tablet, Smart TV, Game console etc.), operating system and client SW type (browser, e-mail client etc.).

### Requirements
PHP 5.3 or later.

### Features
- Fast
- Standalone
- Auto updated datafile and cache from remote server with version checking and checksum datafile
- Released under the GNU (LGPL v.3)

### Install

    composer install

### Usage
You should review the included examples (`parse.php`, `isbot.php`, `account.php` or `full_example.php`)
Here's a quick example:

```php
require_once __DIR__ . '/vendor/autoload.php';
$parser = new Udger\Parser();
$parser->setDataDir(sys_get_temp_dir() . "/udgercache/");
$parser->setAccessKey('XXXXXX');
$ret = $parser->parse('Mozilla/5.0 (Macintosh; Intel Mac OS X 10_9_4) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/39.0.2171.71 Safari/537.36');
echo "<pre>";
print_r($ret);
echo "</pre>";
```

### Dependencies 
- SQLite3(http://php.net/manual/en/book.sqlite3.php)

### Running tests

    ./vendor/bin/codecept run

### data for parser 
- info: https://udger.com/download/data

### Author
The Udger.com Team (info@udger.com)