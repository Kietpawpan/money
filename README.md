# e-Receipt
1. Items and prices are top secret data, encrypted with an external encryption program, decrypted and evaluated oninput to be the variable value:
```
var x = eval(decrypted.toString(CryptoJS.enc.Utf8));
```
2. I used Javascript to display the HTML elements' values (onload), using the for-loop.
3. The data were stored in variable x as the two dimensional array:
```
var x = [['item 1', price 1], ['item 2', price 2], ..., ['item 3', price 3]];
```
   
