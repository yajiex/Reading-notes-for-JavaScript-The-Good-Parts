# Chapter 7: Regular Expressions
* The methods that work with regular expressions are `regexp.exec`, `regexp.test`, `string.match`, `string.replace`, `string.search`, and `string.split`.
* The `(?:...)?` indicates an optional noncapturing group. It is usually better to use noncapturing groups instead of the less ugly capturing groups because capturing has a performance penalty. Noncapturing groups do not interfere with the numbering of capturing groups.
* A regexp choice contains one or more regexp sequences. It attempts to match each of the sequences in order. So: `"into".match(/in|int/)` matches the in in into. It wouldn't match int because the match of in was successful.
* Make a regular expression object that matches
      // a JavaScript string.
      var my_regexp = /"(?:\\.|[^\\\"])*"/g;
* 

