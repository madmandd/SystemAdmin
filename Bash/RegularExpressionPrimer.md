# Regular Expression Primer

The `grep` command searches the content of the files for a given pattern
and prints any line where the pattern is matched. To use `grep`, you need to provide
it with a pattern and one or more filename (or piped data).

|-|-|
|arg|des|
|-|-|
|-c| count the number of lines that match the pattern|
|-E| enable extended regular expressions|
|-f| read the search pattern from a provided file. a file can contain more than one pattern, with each line containing a single pattern |
|-i| ignore character case|
|-l| print only the filename and path where the pattern was found|
|-n| print the line number of the file where the pattern was found|
|-P| enable the perl regular expression engine |
|-R,-r| recursively search subdirectories |

### `grep` and `egrep`

the `grep` command supports some variations, notably extended syntax for the regex patterns
There are three ways to tell `grep` that you want special meaning on certain characters:

1. by preceding those characters with a backslash
2. by telling `grep` that you want special syntax (without the need for a backslash)
   by using -E option when you invoke grep
3. by using the command named `egrep`, which is a script that simply invokes as `grep -E` so you
   don't have to
