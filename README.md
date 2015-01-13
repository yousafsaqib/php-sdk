# Constant Contact PHP SDK
[![Build Status](https://secure.travis-ci.org/constantcontact/php-sdk.png?branch=master)](http://travis-ci.org/constantcontact/php-sdk) [![Latest Stable Version](https://poser.pugx.org/constantcontact/constantcontact/v/stable.svg)](https://packagist.org/packages/constantcontact/constantcontact) [![Latest Unstable Version](https://poser.pugx.org/constantcontact/constantcontact/v/unstable.svg)](https://packagist.org/packages/constantcontact/constantcontact)

### This library utilizes [GuzzlePHP](https://guzzlephp.org)

## Installing via Composer (recommended)
Composer is a dependency management tool for PHP that allows you to declare the dependencies your project needs and installs them into your project. In order to use the Constant Contact PHP SDK through composer, you must do the following 

1. Add "constantcontact/constantcontact" as a dependency in your project's composer.json file.
```javascript
 {
        "require": {
            "constantcontact/constantcontact": "2.0.*"
        }
    }
```

2. Download and Install Composer.
```
curl -s "http://getcomposer.org/installer" | php
```

3. Install your dependencies by executing the following in your project root.
```
php composer.phar install
```

4. Require Composer's autoloader.
Composer also prepares an autoload file that's capable of autoloading all of the classes in any of the libraries that it downloads. To use it, just add the following line to your code's bootstrap process.
```
require 'vendor/autoload.php';
```

### Manual Installation
1. Download and extract the project into an appropriate place in your application.
2. Require the SDK's autoloader. (note: the path to include the autoload may be different depending on the structure of your application)
```
require '/src/Ctct/autoload.php'
```


## Usage
Once either the composer or built in autoloader has been required, you can begin using the SDK.
```php
use Ctct\ConstantContact;
$cc = new ConstantContact('your api key');

$contacts = $cc->getContacts('your access token')
```
## Minimum Requirements
Use of this library requires PHP 5.4+, and PHP cURL extension (http://php.net/manual/en/book.curl.php)
