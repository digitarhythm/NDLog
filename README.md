# NDLog
console log like NSLog

## Usage(CoffeeScript)
----
foo = "123"  
bar = "456"  
echo = require("ndlog").echo  
echo("foo=%@, bar=%@", foo, bar)  

foo = "abc"  
bar = "def"  
form = require("ndlog").form  
str = form("foo=%@, bar=%@", foo, bar)  
console.log(str)
----

 foo=123, bar=456
 foo=abc, bar=def

## explain
'echo' is dispay format string when 'NODE_ENV' environment is 'develop'.
'form' is return format string.
zero binding number return 'form' method.
ex)
echo("foo=%05@", 12) -> 00012

