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

Hence the coding style presented here can be used as an alternative to PSR-2. It is simpler and presents some code examples. We point out the differences between the guidelines during their definition, so take a look and make your conclusions.

### Example

The following piece of code is the same presented in PSR-2, [here](http://www.php-fig.org/psr/psr-2/#1-1-example), but uses our coding style.

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

  public static final function bar() {
    // method body
  }
  
}
```

### Overview

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](http://www.ietf.org/rfc/rfc2119.txt).

1. Code MUST follow the [PSR-1](http://www.php-fig.org/psr/psr-1/) "coding style guide"; _(same as PSR-2)_
2. Code MUST tabs for indenting, not spaces. Tab size MUST be equivalent to 4 spaces; _(different from PSR-2)_
3. There MUST NOT be a hard limit on line length; the soft limit MUST be 120 characters; lines SHOULD be 80 characters or less;  _(same as PSR-2)_
4. There MUST be one blank line after the declaration of:
  - `namespace`s; _(same as PSR-2)_
  - `use`s;  _(same as PSR-2)_
  - `class`es; _(different from PSR-2)_
5. Opening braces MUST go on the same line, and closing braces MUST go on the next line after the body, for any code constructions; _(different from PSR-2)_
6. One blank space MUST be placed:
  - After control structures; _(same as PSR-2)_
  - After opening parenthesis; _(different from PSR-2)_
  - Before closing parenthesis; _(different from PSR-2)_
  - After comma; _(not defined in PSR-2)_
7. Methods and function calls MUST NOT have one space after them; _(same as PSR-2)_
8. Visibility MAY be declared on all properties and methods (PHP assumes `public` as the default visibility); _(different from PSR-2)_
9. `abstract`, `final` and `static` MUST be declared _after_ the visibility, and `static` MUST be declared _after_ `final`; _(different from PSR-2)_
