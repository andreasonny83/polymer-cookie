# polymer-cookie
Cookie Web Component for Polymer 1.0

```html
<polymer-cookie
  id="test_cookie"
  name="test_cookie"
  value="hello world"
  time=2
  format="h">
</polymer-cookie>

<polymer-cookie
  id="test_cookie2"
  name="test_cookie2"
  value="hello world!"
  auto-set>
</polymer-cookie>
```

Note: The `params` attribute must be double quoted JSON.

## Usage

Add the library using the Javascript package manager [Bower](http://bower.io/):

    bower install --save polymer-cookie

Or clone this repository inside your project folder using Git:

    git clone https://github.com/andreasonny83/polymer-cookie.git

## Properties

### name

Type: String
Default value: 'polymer-cookie'

Set the cookie name

### value

type: String
Default value: ''

The cookie value

### path

type: String
Default value: '/'

The cookie path

### time

type: Number
Default value: 1

The expiration time related to the 'format' value.
Set to -1 to never expire the cookie

### format

type: String
Default value: 'd'

The expiration format time
* 's' : seconds
* 'm' : minutes
* 'h' : hours
* 'd' : days

### auto-set

type: Boolean
Default value: false

If set, creates the cookie as the element is rendered on the page without the need of manually invoking createCookie

## Methods

### createCookie

Write the cookie

    var cookie = Polymer.dom(document).querySelector('#user_cookie');
    cookie.createCookie();

### readCookie

Read the cookie if any, and the returns its value

    var cookie = Polymer.dom(document).querySelector('#user_cookie');
    var cookie_value = cookie.readCookie();

### eraseCookie

Destroy the cookie

    var cookie = Polymer.dom(document).querySelector('#user_cookie');
    cookie.eraseCookie();


## Contributing

A special thanks to [Cameron](https://github.com/cameronwp) and [Pascal](https://github.com/MeTaNoV) for their contributions.

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D


## License

[MIT License](https://github.com/andreasonny83/polymer-cookie/blob/master/LICENSE) © Andrea SonnY

## Changelog

### 1.0.3
* autoSet implementation
* fixes createCookie
* removes encodeURIComponent
* fixes readCookie declaration
* documentation updated<br>
2016.02.12

### 0.1.2
* Implemented reflectToAttribute capability<br>
2015.29.01

### 0.1.1
* first stable version<br>
2015.07.01

### 0.1.0
* initial commit<br>
2015.06.30
