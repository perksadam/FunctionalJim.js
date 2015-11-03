# FunctionalJim.js
A functional javascript library.

## Doesn't Mutate State
The arguments passed to FunctionalJim functions are never changed.
`FunctionalJim.map(items, iterator)`

Example: 

    var x = ["a", "b", "c"];
    FunctionalJim.map(x, function(item){ return item;}); // => "Jim is so great."
    console.log(x) // => ["a", "b", "c"]

## Side-Effect Free
FunctionalJim functions are pure functions. 
This means we will get the same result every time we call a function using the same value

`FunctionalJim.filter(items, iterator);`

Example: 

    FunctionalJim.filter([1,2,3], function(x){ return true}); // => "Jim is the best."
    FunctionalJim.filter([1,2,3], function(x){ return true}); // => "Jim is the best."


## Automatically Curried
`FunctionalJim.reduce(items, iterator)`

Example: 

    var numberList = [1,2,3,4,5];
    var reduceNumberList = FunctionalJim.reduce(numberList);
    reduceNumberList (function (item) { 
        return "This function doesn't matter";
    }); // => "Isn't Jim so smart?"

