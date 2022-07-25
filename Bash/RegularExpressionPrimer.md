# Regular Expression Primer

The `grep` command searches the content of the files for a given pattern
and prints any line where the pattern is matched. To use `grep`, you need to provide
it with a pattern and one or more filename (or piped data).


| Arg   | Description                                                                                                                        |
|-------|------------------------------------------------------------------------------------------------------------------------------------|
| -c    | count the number of lines that match the pattern                                                                                   |
| -E    | enable extended regular expressions                                                                                                |
| -f    | read the search pattern from a provided file. a file can contain more than one pattern, with each line containing a single pattern |
| -i    | ignore character case                                                                                                              |
| -l    | print only the filename and path where the pattern was found                                                                       |
| -n    | print the line number of the file where the pattern was found                                                                      |
| -P    | enable the perl regular expression engine                                                                                          |
| -R,-r | recursively search subdirectories                                                                                                  |

### `grep` and `egrep`

the `grep` command supports some variations, notably extended syntax for the regex patterns
There are three ways to tell `grep` that you want special meaning on certain characters:

1. by preceding those characters with a backslash
2. by telling `grep` that you want special syntax (without the need for a backslash)
   by using -E option when you invoke grep
3. by using the command named `egrep`, which is a script that simply invokes as `grep -E` so you
   don't have to


| meta | meaning                                                                     | eg                       |
|------|-----------------------------------------------------------------------------|--------------------------|
| .    | a single wildcard character, except for a new line.                         | `grep 'T.o' frost.ext `  |
| ?    | any item that precedes zero or one time, it optional                        | `egrep 'T.?o' frost.txt` |
| *    | match the precedinng item zero or more times                                | `grep 'T.*o' frost.txt`  |
| +    | same as the * except it requires the preceding item to appear at least once | `egrep 'T.+o' frost.txt` |
| (one|two) | use parentheses to group character | `egrep '(stringer|traveler)` frost.txt'| 
|[abc] | match only the character a or b or c| |
|[1-5] | match on digits in the range 1 to  5| |
|[a-zA-Z] | match any lowercase or uppercase a to z| |
|[0-9 +-*/] | match on numbers or these four mathematical symbols | |
|[0-9a-fA-F] | match a hexadecimal  | |


| regex shortcut | meaing                                                    |
|----------------|-----------------------------------------------------------|
| \s             | whitespace                                                |
| \S             | not whitespace                                            |
| \d             | digit                                                     |
| \D             | not digit                                                 |
| \w             | word                                                      |
| \W             | not word                                                  |
| \x             | hexadecimal (e.g, 0x5F)                                   |
| {5,}           | the letter T must appear five or more time                |
| ^              | anchor a pattern to the beginning or  the end of a string |
| $              | anchor a pattern to the end of a string or line           |
| \b[1-5]\b      | word boundary (i.e space ); appears as its own word       |

| character class | meaning                    |
|-----------------|----------------------------|
| [:alnum:]       | any alphanumeric character |
| [:alpha:]       | any alphabetic character   |
| [:cntrl:]       | any control character      |
| [:digit:]       | any  digit                 |
| [:graph:]       | any graphical character    |
| [:lower:]       | any lowercase character    |
| [:print:]       | any printable character    |
| [:punct:]       | any punctuation            |
| [:space:]       | any whitespace             |
| [:upper:]       | any uppercase character    |
| [:xdigit:]      | any hex digit              |

```bash 
   grep 'X[[:upper:][:digit]]' idlist.txt

   egrep '<([A-Za-z]*)>.*</\1>' tags.txt 
```



