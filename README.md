# Mask documentation

This mask function has no dependencies, it works on all major browser and allows you to create any mask simply.

```js
// how to mask a field to a date format 
window.mask(inputRef, "NN/NN/NNNN"); 
```

```js
// how to mask a field to a currency format 
window.mask(inputRef, "NNN.NNN.NN", true); //the last argument tells that this is a numeric field  
```

The function has only tree arguments.

- The first is the reference to the input. You can get that by using plain Dom or jQuery

Using Dom:
```js
var inputRef = document.forms[0].inputName;
window.mask(inputRef, "NN/NN/NNNN"); 
```

Using jQuery:
```js
var inputRef = $("#inputID")[0];
window.mask(inputRef, "NN/NN/NNNN"); 
```

- The second argument is the mask. You can configure the mask using a few letters and simbols. This function will recogzine the following letters to mask the field:

       - C - For characteres 
       - N - For numbers
       - A - For characteres and numbers
       - S - For simbols
       - Z - For anything

So, if you are masking a field for a canadian Zip Code, the mask would be:

```js
window.mask(inputRef, "CNC-NCN"); 
```

- The last argument is a flag to indicate that the field is numeric. This will make the field to be aligned by right and will allow the user to type negative values. A field to insert weight:

```js
window.mask(inputRef, "NNNN.NN", true);   
```

Examples: https://codepen.io/ivanvaladares/pen/jZvbXz

