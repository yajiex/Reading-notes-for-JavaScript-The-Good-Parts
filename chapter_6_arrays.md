# Chapter 6: Arrays
* JavaScript doesn't have **real** kind of array, it just provides an object that has some array-like characteristics. Retrieval and updating of properties work the same as with objects, except that there is a special trick with integer property names.
* If you store an element with a subscript that is greater than or equal to the current `length`, the length will increase to contain the new element. There is no array bounds error
* The `[]` postfix subscript operator converts its expression to a string using the expression's `toString` method if it has one.
* Making the `length` larger does not allocate more space for the array. Making the `length` smaller will cause all properties with a subscript that is greater than or equal to the new `length` to be deleted
* Since JavaScript's arrays are really objects, the `delete` operator can be used to remove elements from an array. Unfortunately, that leaves a hole in the array. This is because the elements to the right of the deleted element retain their original names
* JavaScript arrays have a `splice` method. It can do surgery on an array, deleting some number of elements and replacing them with other elements. Because every property after the deleted property must be removed and reinserted with a new key, this might not go quickly for large arrays.
* The `for in` statement can be used to iterate over all of the properties of an array, unfortunately it makes no guarantee about the order of the properties, Also, there is still the problem with unexpected properties being dredged up from the prototype chain.
* The `typeof` operator reports that the type of an `array` is `'object'`, which isn't very helpful.
* A polyfill for accurately detecting array:
      var is_array = function (value) {
          return value && typeof value === 'object' && value.constructor === Array;
      };


