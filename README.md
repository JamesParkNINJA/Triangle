#Retired, due to monitisation of needed resources.

---

# benjamin.js
A jQuery currency converter, formatter, and symbol applier. All about the Benjamins, baby!

Currently works with:

AUD, BGN, BRL, CAD, CHF, CNY, CZK, DKK, GBP, HKD, HRK, HUF, IDR, ILS, INR, JPY, KRW, MXN, MYR, NOK, NZD, PHP, PLN, RON, RUB, SEK, SGD, THB, TRY, USD, and ZAR

Like what I do? [Donate me a beer!](https://www.paypal.me/jamesparkninja/4)

## Using the plugin

### Markup

```html
<!-- Standard setup for single class -->
<span class="benjamin">£55.40</span>

<!-- "data-oldbj": Override the oldCurrency option in your main JS call -->
<!-- "data-newbj": Override the newCurrency option in your main JS call -->
<span class="benjamin" data-oldbj="GBP" data-newbj="USD">£3456.99</span>

<!-- Setup for all elements within container -->
<div class="benjaminContainer">
    <span>$5,655.80</span>
    <span>$455.46</span>
    <span>$33,334.00</span>
</div>
```


```javascript
$(document).ready(function ($) {
    // Only select elements with specific class
    $('.benjamin').benjaminjs(
        {
            oldCurrency: 'GBP', // The current currency used (to convert FROM)
            newCurrency: 'EUR' // The new proposed currency (to convert TO)
        }
    );
    
    // Used for all span elements within a container
    $('.benjaminContainer span').benjaminjs(
        {
            oldCurrency: 'USD',
            newCurrency: 'GBP'
        }
    );
});
```


## API Dependencies

* [WebServiceX](http://www.webservicex.net/) - Currency Rates API

## Removed Dependencies

* [Fixer.io](http://fixer.io/) - Sadly switched to a paid-for SAAS API, no longer viable.

## Authors

* **James Park** - *Initial work* - [JamesPark.ninja](https://github.com/JamesParkNINJA)

## License

This project is licensed under the MIT License

## Acknowledgments

* Thank you StackOverflow
