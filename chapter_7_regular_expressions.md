# Chapter 7: Regular Expressions
* The methods that work with regular expressions are `regexp.exec`, `regexp.test`, `string.match`, `string.replace`, `string.search`, and `string.split`.
* The `(?:...)?` indicates an optional noncapturing group. It is usually better to use noncapturing groups instead of the less ugly capturing groups because capturing has a performance penalty. Noncapturing groups do not interfere with the numbering of capturing groups.
* A regexp choice contains one or more regexp sequences. It attempts to match each of the sequences in order. So: `"into".match(/in|int/)` matches the in in into. It wouldn't match int because the match of in was successful.
* A regexp factor may have a regexp quantifier suffix that determines how many times the factor should match. Matching tends to be greedy, matching as many repetitions as possible up to the limit, if there is one. If the quantifier has an extra ? suffix, then matching tends to be lazy, attempting to match as few repetitions as possible. It is usually best to stick with the greedy matching.
* Make a regular expression object that matches
      // a JavaScript string.
      var my_regexp = /"(?:\\.|[^\\\"])*"/g;

