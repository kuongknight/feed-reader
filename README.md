# feed-reader
A node package for handling ATOM/RSS resources and normalize to JSON object.

 [![NPM](https://badge.fury.io/js/feed-reader.svg)](https://badge.fury.io/js/feed-reader)
[![Build Status](https://travis-ci.org/ndaidong/feed-reader.svg?branch=master)](https://travis-ci.org/ndaidong/feed-reader)
 [![Coverage Status](https://coveralls.io/repos/github/ndaidong/feed-reader/badge.svg?branch=master)](https://coveralls.io/github/ndaidong/feed-reader?branch=master)
 [![Dependency Status](https://gemnasium.com/badges/github.com/ndaidong/feed-reader.svg)](https://gemnasium.com/github.com/ndaidong/feed-reader)
 [![Known Vulnerabilities](https://snyk.io/test/npm/feed-reader/badge.svg)](https://snyk.io/test/npm/feed-reader)

### API & Usage

```
npm install feed-reader
```

This module provides only one method:

- .parse(String feedURL)

In which, feedURL is the url to RSS or ATOM resource.

For example:

```
var reader = require('feed-reader');
reader.parse(SOME_RSS_URL);
```

Result is a Promise. View the example below for more detail:

```
var parse = require('feed-reader').parse;

let url = 'https://news.google.com/news/feeds?pz=1&cf=all&ned=us&hl=en&q=nodejs&output=rss';

parse(url).then((feed) => {
  console.log(feed);
}).catch((err) => {
  console.log(err);
}).finally(() => {
  console.log('Everything done');
});
```


## Test

```
git clone https://github.com/ndaidong/feed-reader.git
cd feed-reader
npm install
npm test
```


# License

The MIT License (MIT)
