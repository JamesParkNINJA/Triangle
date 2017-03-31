# benjamin.js
A jQuery currency converter, formatter, and symbol applier. All about the Benjamins, baby!

## Using the plugin

### Markup

```html
<span class="benjamin">£55.40</span>

<span class="benjamin" data-oldbj="GBP" data-newbj="USD">£3456.99</span>

<div class="benjaminContainer">
    <span>$5,655.80</span>
    <span>$455.46</span>
    <span>$33,334.00</span>
</div>
```


```javascript
$(document).ready(function ($) {
    $('.benjamin').benjaminjs(
        {
            oldCurrency: 'GBP',
            newCurrency: 'EUR'
        }
    );
    
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

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Thank you StackOverflow