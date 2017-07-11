# NDLog
console log like NSLog

## Usage(CoffeeScript)
    
    echo = require("ndlog").echo
    form = require("ndlog").form
    
    foo = "123"
    bar = "456"
    echo("foo=%@, bar=%@", foo, bar)
    
    foo = "abc"
    bar = "def"
    str = form("foo=%@, bar=%@", foo, bar)
    console.log(str)

## output
    foo=123, bar=456
    foo=abc, bar=def

## explain
    'echo' is string display when 'NODE_ENV' environment is 'develop'.
     Not display when 'NODE_ENV' is not 'develop'.
     'form' is return format string.
     'form' is return zero binding number too.
     Write "%@" in the place where you want to display the variable.

## examplle
    echo("foo=%@", "abc") -> foo=abc
    echo("bar=%05@", 12) -> bar=00012

