# Chapter 5: Inheritance
* When a function object is created, the `Function` constructor that produces the function object runs some code like this: `this.prototype = {constructor: this};` The new function object is given a `prototype` property whose value is an object containing a `constructor` property whose value is the new function object.
* Module Pattern:
  1. It creates a new object
  2. It optionally defines private instance variables and methods
  3. It augments that new object with methods
  4. It returns that new object
  
  Here is a pseudocode template:
      var constructor = function (spec, my) {
          var that, other private instance variables;
          my = my || {};
          Add shared variables and functions to my
          that = a new object;
          Add privileged methods to that
          return that;
      };
      
      var mammal = function (spec) {
          var that = {};
          that.get_name = function ( ) {
              return spec.name;
          };
          that.says = function ( ) {
              return spec.saying || '';
          };
          return that;
      };
      var myMammal = mammal({name: 'Herb'});
* 
