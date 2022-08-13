# Japan Postal code oasis

JavaScript module for Japan Postal Code.

Forked from https://github.com/mzp/japan-postal-code

## Features

* ES6 modules
* Promise
* No dependency
* Customize data url(must host yourself)
* Bundle version (WIP)

## How to install

```
npm install japan-postal-code-oasis
```

## How to use

```js
const postal = import 'japan-postal-code-oasis';

const DATA_URI_BASE = 'https://example.com/path/to/data/';
// Update the URL to the base URL of your JSON data files

postal.configure(DATA_URI_BASE);

postal('1000001').then(address => {
  console.log(address.prefecture); // => "東京都"
  console.log(address.city); // => "千代田区"
  console.log(address.area); // => "千代田"
  console.log(address.street); // => ""
});
```

or

```js
const postal = import 'japan-postal-code-oasis';

const DATA_URI_BASE = 'https://example.com/path/to/data/';
// Update the URL to the base URL of your JSON data files

postal('1000001', DATA_URI_BASE).then(address => {
  console.log(address.prefecture); // => "東京都"
  console.log(address.city); // => "千代田区"
  console.log(address.area); // => "千代田"
  console.log(address.street); // => ""
});
```

## LICENSE
MIT License
