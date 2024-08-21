# e-Receipt
Items and prices are top secret data, encrypted with an external program, decrypted on input and evaluated to be the variable value:
```
var x = eval(decrypted.toString(CryptoJS.enc.Utf8));
```
