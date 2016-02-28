# effective-php-coding-style
An effective PHP coding style, based on the PSR-1. It can be used as an alternative to the PSR-2.

Current [version](http://semver.org/): `0.1` _(under construction)_

### Translations

- [Brazilian Portuguese](README-PT-BR.md) **SOON!**

### About

PHP-FIG's [PSR-1](http://www.php-fig.org/psr/psr-1/) presents a good _basic coding standard_ for PHP applications and does not impose a style.
However, the [PSR-2](http://www.php-fig.org/psr/psr-2/) _coding style guide_ has some **inconvenient** guidelines such as:

* It recommends the use of spaces instead of TABs;
* Opening braces start in a new line instead of starting in the same line;
* Opening parentheses for control structures do not have a pharentheses after them.
* _etc._

Hence the coding style presented here can be used as an alternative to PSR-2. It is simpler, presents some code examples and have a different structure. We point out the differences between the guidelines during their definition, so take a look and make your conclusions.

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
?>
```

# The Coding Style

## General

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](http://www.ietf.org/rfc/rfc2119.txt).

1. Code MUST follow the [PSR-1](http://www.php-fig.org/psr/psr-1/) "coding style guide"; _(same as PSR-2)_

## Naming

1. Directories MUST use dashed-case (examples: `api`, `sample-code`); _(not defined in PSR-2)_
2. PHP files MUST be named with the `.php` extension. You MAY use `.class.php` or `.inc.php` but this is NOT RECOMMENDED; _(not defined in PSR-2)_
3. Files that contain classes MUST be named using the main class' name (example: `MyImportantClass.php`);
4. Files that do not containt classes MUST be named in dashed-case (example: `hello-world.php`)

## Lines

1. Files MAY use _any_ line-ending (Windows, Unix or Mac). However, all project files SHOULD use the same line-ending; _(different from PSR-2)_
2. There MUST NOT be a hard limit on line length; the soft limit MUST be 120 characters; lines SHOULD be 80 characters or less;  _(same as PSR-2)_

## Code

### Identing

1. Code MUST use _tabs_ for indenting, not spaces. Tab size MUST be equivalent to 4 spaces; _(different from PSR-2)_

### Blanks lines

1. There MUST be one blank line after the declaration of:
  1. `namespace`s; _(same as PSR-2)_
  2. `use`s;  _(same as PSR-2)_
  3. `class`es; _(different from PSR-2)_
  4. between methods or functions; _(not defined in PSR-2)_

### Blank spaces

1. There MUST be one blank space:
  1. After control structures; _(same as PSR-2)_
  2. After opening parenthesis; _(different from PSR-2)_
  3. Before closing parenthesis; _(different from PSR-2)_
  4. Before and after the following operators:  _(not defined in PSR-2)_
  	1. [Arithmetic operators](http://php.net/manual/en/language.operators.arithmetic.php), except for negation (e.g. `-$x`);
  	2. [Assignment operators](http://php.net/manual/en/language.operators.assignment.php);
  	3. [Bitwise operators](http://php.net/manual/en/language.operators.bitwise.php);
  	4. [Comparison operators](http://php.net/manual/en/language.operators.comparison.php);
  	5. [Logical operators](http://php.net/manual/en/language.operators.logical.php);
  	6. [String operators](http://php.net/manual/en/language.operators.string.php);
  	7. [Array operators](http://php.net/manual/en/language.operators.array.php);
  	8. [Type operators](http://php.net/manual/en/language.operators.type.php);
  5. After comma; _(not defined in PSR-2)_
2. Methods and function calls MUST NOT have one blank space after them; _(same as PSR-2)_

### Braces

1. Opening braces MUST go on the same line, and closing braces MUST go on the next line after the body, for any code constructions; _(different from PSR-2)_

### The Language

1. PHP [keywords](http://php.net/manual/en/reserved.keywords.php) MUST be in lower case;  _(same as PSR-2)_
2. The PHP constants `true`, `false`, and `null` MUST be in lower case;  _(same as PSR-2)_
3. Constants MUST be declared using upppercase letters and snake_case. Example: `MAX_ENERGY`.  _(same as PSR-2)_
3. Visibility MAY be declared on properties and methods (PHP assumes `public` as the default visibility); _(different from PSR-2)_
4. `abstract`, `final` and `static` MUST be declared _after_ the visibility, and `static` MUST be declared _after_ `final`; _(different from PSR-2)_
