# <img src="public/ystorian.svg" style="height:1em;"> Ystorian URL Shortener

URL shortener app for [Ystorian](https://www.ystorian.com).

Project stopped since Chrome complains about [⬣.tk](https://⬣.tk) being a potential unsafe site, due to:
* International Domain Names (IDN) with emoji encoded as punny code (⬣.tk is encoded as xn--45i.tk)
* dotTK (.tk) domains have a bad reputation.

This repository and the site are kept to test various security headers and configurations.


## Content Security Policy (CSP)
### Inline script
To get the sha384 hash of the script and style, encoded as a base-64 string, select the text between the tags (including tabs and whitespace), copy, and type this command (macOS):

```shell
pbpaste | openssl sha384 -binary | openssl base64
```

### Third party script
Get the hash:
```shell
curl -s https://plausible.io/js/plausible.js | openssl dgst -sha384 -binary | openssl base64
```

Then add the hash in the script tag:
```html
<script ...
	src="https://plausible.io/js/plausible.js"
	integrity="sha384-0tX/C66trbqI1ludXxeZmlfZv7n7W+SsSI45FPLHoK49MIpj6t7dyZ7CalV7x2pk"
	crossorigin="anonymous"></script>
```


## Sources
* Font: [Lato](https://www.latofonts.com/lato-free-fonts/) for devices without a thin font like Helvetica Neue.
* SVG: Ystorian logo by Flavien Scheurer
* JS: Code inspiration from:
  * [How to Build a Clock with JavaScript and SVG](https://www.section.io/engineering-education/how-to-build-a-clock-with-javascript-and-svg/) by [Olubisi Idris Ayinde](https://github.com/Olanetsoft)
  * [An SVG Analog Clock In 6 Lines of JavaScript](http://thenewcode.com/943/An-SVG-Analog-Clock-In-6-Lines-of-JavaScript) by [Dudley Storey](https://twitter.com/dudleystorey)
