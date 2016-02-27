# effective-php-coding-style
An effective PHP coding style, based on the PSR-1. It can be used as an alternative to the PSR-2.

Current [version](http://semver.org/): `1.0`

### Translations

- [Brazilian Portuguese](README-PT-BR.md)

### About

PHP-FIG's [PSR-1](http://www.php-fig.org/psr/psr-1/) presents a good _basic coding standard_ for PHP applications and does not impose a style.
However, the [PSR-2](http://www.php-fig.org/psr/psr-2/) _coding style guide_ has some **inconvenient** guidelines such as:

* It recommends the use of spaces instead of TABs;
* Opening braces start in a new line instead of starting in the same line;
* Opening parentheses for control structures do not have a pharentheses after them.
* _etc._

Hence the coding style presented here can be used as an alternative to PSR-2. We point out the differences between the guidelines during their definition, so take a look and make your conclusions.

### Example

```php
<?php
namespace Vendor\Package;

use FooInterface;
use BarClass as Bar;
use OtherVendor\OtherPackage\BazClass;

class Foo extends Bar implements FooInterface {

  public function sampleFunction( $a, $b = null ) {
    if ( $a === $b ) {
      bar();
    } else if ( $a > $b ) {
      $foo->bar( $arg1 );
    } else {
      BazClass::bar( $arg2, $arg3 );
    }
  }

  final public static function bar() {
    // method body
  }
  
}
```
