# e-Receipt
e-Receipt is a classified e-receipt, of which the items and prices can be accessed with a secret key. The data have been encrypted with the Advanced Encryption Standard implemented in the JavaScript library: crypto.js.

## How to Use
1. Open [e-Receipt](https://kietpawpan.github.io/money/)
2. Enter the secret key.
3. The encrypted data will be decrypted and shown up.

## How to edit
Given you have a new item and its price to be included in the [e-Receipt](https://kietpawpan.github.io/money/), you can do as follows:
1. Open the index.html file.
2. Copy and paste this code beneath the last item.:
```E
<div class="transactionDetails">
<div class="detail" id="an"></div>
<div class="detail" id="jn" type="text"></div>
</div>
```
3. Edit the div id values:
> [!Note]
> "an" and "jn" are the id values for the divisions of the new item and the new price, respectively.

4. Copy the current cipher text:
```
U2FsdGVkX18lLSq1grR569u8l621WOmlAZgCpp8TDUJDQhdvIkTuVCHtTrTDqtrMg4Z80yooZNw9V01AIJBHNinLcl2BHg0eack8xkZS/VtDr3BrluQ0gAC0HpBoSlPrSj92mh2mGmb9wwz8SwhGACUCy0w66qi9CYa3nwlmkiZqSlPWddp9yhZCbXa8BPXGJDKcVdZZrMP7ghoIwuEz/wp2ffSCicyAGTZ027Nnp0PPqf8PHridEssN26rHzdBQ1/6lPew6/dJW1oLcOxQLlrct4UY6Z0F0zRoJc0rayiwXNTlzQPyJ20EbUjFX4P+bqjaU42xeZe4o77EOboS7F3dlXdtEAPbSBJ5W7DGeMf3YzWhh+TFI1ahAuNQs/e5Rn9yCs8eutUpMZDChJIdwCV3U4GVkjFovagW8+dd1sBPo1b8PUdgIg1bGQ/3fyuZgQVTeQnhLnPVyYJ/uQpTIUkoF2D9Xo1Aq9H11QiTj8uRSM9Ep8WYsQgnuqt8wm76cBWUW2DwRvknW4OB06X7UcspGlDD/cOQS04Wa6mCD/ASSjOcRXmicFfos0UVB/DHPpIkisPHT3bKWZGl6fsufMkZp1rnp4n9JWnHebh7AbCog7Po884qXxNKsxiyh9GErYGcPJj73TtOn/ojlHJn4nTTt/V4/mC2xXQ4odDvNBMaqD+25F5l3AI7i5Quo/CO+ftaOLcrm5dma+8+EuovDlGFRhVUg2lkorQRHcd//Yg+ZbXvhtgq4uSF14vUhcxqYP8MqjZH1mFTJ0o29iIlE/LOZUYIg5IOV1W8UPMuNqyLs2puP/yihm+hy3rwkSETPhSALObfVfQoIncytwFpAKgwqvEHH4y60j3pCJzOoQy4BsxRq9k32l9h+77eG7pSqu/hQ7qJ3hjumDR2iaTxVvnvYKpU6aHGk/4BXb6mkqMu2WW66uJK4gGIR3r3CbJOH8Buj2ZAXJiYinUiZcF0cRJUDXElhULQykMOMXGISjww=
```
5. Go to [https://kietpawpan.github.io/encryption](https://kietpawpan.github.io/encryption/) and paste the cipher text into the cipher text input box.
6. Type the secret key in the secret key input box.
7. Click the Decrypt button. The decrypted data will be a two-dimensional array.
```
 [['item 1', price 1], ['item 2', price 2], ..., ['item 3', price 3]]
```
9. Click the clone icon.
10. Paste the decrypted data into the classified data input box.
11. Edit the array, by adding the new pair of item and price.
```
 [['item 1', price 1], ['item 2', price 2], ..., ['item 3', price 3]], ['new item', new price]]
```
12. Encrypt it with the same web app.
13. Copy the new cipher text.
14. Replace the old cipher text with the new one.

## Coding Note
1. A decrypted text can be set as a variable value by using eval().
```
var x = eval(decrypted.toString(CryptoJS.enc.Utf8));
```
2. A for loop was used for displaying the HTML elements' values (onload).
```
for(let y=0; y<x.length;y++){
  document.getElementById("a"+y).innerHTML = x[y][0];
  document.getElementById("j"+y).innerHTML = x[y][1];
}
```
4. The data were stored in variable x as the two dimensional array:
```
var x = [['item 1', price 1], ['item 2', price 2], ..., ['item 3', price 3]];
```
> [!NOTE]
> Array references
```
         column 0  column 1
  row 0  x[0][0]   x[0][1]
  row 1  x[1][0]   x[1][1]
  row y  x[y][0]   x[y][1]
          item     price
```
