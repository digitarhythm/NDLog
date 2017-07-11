# NDLog
console log like NSLog

## Usage(CoffeeScript)
`
echo = require("ndlog").echo
form = require("ndlog").form

foo = "123"
bar = "456"
echo("foo=%@, bar=%@", foo, bar)

foo = "abc"
bar = "def"
str = form("foo=%@, bar=%@", foo, bar)
console.log(str)
`
foo=123, bar=456
foo=abc, bar=def

## explain
'echo' is dispay format string when 'NODE_ENV' environment is 'develop'.
'form' is return format string.
zero binding number return 'form' method.
ex)
echo("foo=%05@", 12) -> 00012

