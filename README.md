# benjamin.js
A jQuery currency converter, formatter, and symbol applier. All about the Benjamins, baby!

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

* [Fixer.io](http://fixer.io/) - Main Currency Rates API (High up-rate)
* [WebServiceX](http://www.webservicex.net/) - Backup Currency Rates API (Lower up-rate)

## Authors

* **James Park** - *Initial work* - [JamesPark.ninja](https://github.com/JamesParkNINJA)

## License

This project is licensed under the MIT License

## Acknowledgments

* Thank you StackOverflow