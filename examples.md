# Examples

## class, interface, trait, method, function

Interfaces and traits follow the same rules as classes. Functions follow the same rules as methods.

```php
namespace Vendor\Package;

use FooInterface;
use BarClass as Bar;
use OtherVendor\OtherPackage\BazClass;

class Foo extends Bar implements FooInterface {

	const X = 0;
	private $any;
	
	function __constructor() {
		$this->any = self::X;
	}

    public function sampleFunction( $a, $b = null ) {
        // method body
    }

    public static final function bar( Foo &$obj ) {
        return $obj->sampleFunction( $a );
    }

}
```

## closure

```php
$closureWithArgs = function ( $arg1, $arg2 ) {
    // body
};

$closureWithArgsAndVars = function ( $arg1, $arg2 ) use ( $var1, $var2 ) {
    // body
};
```

## if, else, else if

```php
if ( $a > $b ) {
	// body
} else if ( $b > $c && $a < SOME_CONSTANT ) {
	// body
} else {
	// body
}
```

## switch

```php
switch ( $value ) {
	case 10: {
		$x = 100;
		break;
	}
	case 20: ; // no break
	case 30: ; // no break
	case 40: {
		$x = 200;
		// no break
	}
	case 50: {
		return ++$x;
	}
	default: {
		$x = 0;
	}
}
```

## while, do while

```php
$i = 0;
while ( $i < 100 ) {
	++$i;
}

$i = 0;
do {
	++$i;
} while ( $i < 100 );
```

## for, foreach

```php
for ( $i = 0; $i < 100; ++$i ) {
	// body
}

$ages = array( 'Bob' => 20, 'Suzan' = 19, 'Paul' = 35 );
foreach ( $ages as $name => $age ) {
	echo $name, ' is ', $age, ' years old.';
}
```

## try, catch, finally

```php
$pdo = null;
$result = 'connected!';
try {
	$pdo = new PDO('mysql:host=127.0.0.1;dbname=test', 'root', '' );
} catch ( \PDOException $pe ) {
	$result = 'Database connection error: ' . $e->getMessage();
} finally {
	logMe( $result );
}
```

## operators

```php
$min = $value < 0 ? 0 : $value;
if ( $max < $min || $max === ( $min / 2 ) ) {
	// ...
}
```
