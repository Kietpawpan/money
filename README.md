# e-Receipt
## How to edit
Given you have a new item and its price to be included in the e-Receipt, you can program as follows:
1. Open the index.html file.
2. Copy and paste this code beneath the last item.:
```
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
13. 7. Items and prices are top secret data, encrypted with an external encryption program, decrypted and evaluated oninput to be the variable value:
```
var x = eval(decrypted.toString(CryptoJS.enc.Utf8));
```
2. I used Javascript to display the HTML elements' values (onload), using the for-loop.
3. The data were stored in variable x as the two dimensional array:
```
var x = [['item 1', price 1], ['item 2', price 2], ..., ['item 3', price 3]];
```
   
