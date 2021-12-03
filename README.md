# <img src="public/ystorian.svg" style="height:1em;"> Ystorian URL Shortener

URL shortener app for [Ystorian](https://www.ystorian.com).

Project stopped since Chrome complains about [⬣.tk](https://⬣.tk) being a potential unsafe site, due to:
* International Domain Names (IDN) with emoji encoded as punny code (⬣.tk is encoded as xn--45i.tk)
* dotTK (.tk) domains have a bad reputation.

## Content Security Policy (CSP)
To get the sha256 hash of the script and style, encoded as a base-64 string, select the text between the tags (including tabs and whitespace), copy, and type this command (macOS):

```shell
pbpaste | openssl sha256 -binary | openssl base64
```

## Sources
* Font: [Lato](https://www.latofonts.com/lato-free-fonts/) for devices without a thin font like Helvetica Neue.
* SVG: Ystorian logo by Flavien Scheurer
* JS: Code inspiration from:
  * [How to Build a Clock with JavaScript and SVG](https://www.section.io/engineering-education/how-to-build-a-clock-with-javascript-and-svg/) by [Olubisi Idris Ayinde](https://github.com/Olanetsoft)
  * [An SVG Analog Clock In 6 Lines of JavaScript](http://thenewcode.com/943/An-SVG-Analog-Clock-In-6-Lines-of-JavaScript) by [Dudley Storey](https://twitter.com/dudleystorey)
