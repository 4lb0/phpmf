PHP Method Finder
=================

The PHP functions library is very complete but the lack of standard on the names 
make it hard to use. With method finder you can put the arguments and the expected
result and you'll get the functions that can *return* that result.

For using you just run the `phpmf` file with 2 params the arguments and the expected
result as if they were written in PHP (you should wrapped in quotes).

**phpmf** is based on [Ruby's Method Finder](http://citizen428.net/archives/1585).

## Examples ##

* String functions
        $ ./phpmf  "'uppercase only first'" "'Uppercase only first'"
        ucfirst('uppercase only first') => 'Uppercase only first'

        ./phpmf  "'uppercase only first'" "'Uppercase Only First'"
        ucwords('uppercase only first') => 'Uppercase Only First'

        ./phpmf "'/path/to/some/file.txt'" "'file.txt'"
        basename('/path/to/some/file.txt') => 'file.txt'

* Array function
        $ ./phpmf  "array('a' => 'x', 'b' => 'y')" "array('a','b')"
        array_keys(array (
          'a' => 'x',
          'b' => 'y',
        )) => array (
          0 => 'a',
          1 => 'b',
        )


