# Wappalyzer [![Travis](https://travis-ci.org/aliasio/wappalyzer.svg?branch=master)](https://travis-ci.org/aliasio/wappalyzer/)

[Wappalyzer](https://www.wappalyzer.com) identifies technologies on websites.
It detects content management systems, ecommerce platforms, JavaScript frameworks,
analytics tools and [much more](https://www.wappalyzer.com/technologies).

* [wappalyzer on NPM](https://www.npmjs.com/package/wappalyzer)
* [wappalyzer-core on NPM](https://www.npmjs.com/package/wappalyzer-core)
* [Chrome extension](https://chrome.google.com/webstore/detail/wappalyzer/gppongmhjkpfnbhagpmjfkannfbllamg)
* [Firefox add-on](https://addons.mozilla.org/en-US/firefox/addon/wappalyzer/)
* [Edge extension](https://microsoftedge.microsoft.com/addons/detail/mnbndgmknlpdjdnjfmfcdjoegcckoikn)
* [Bookmarklet](https://www.wappalyzer.com/download)
* [wappalyzer/cli on Docker Hub](https://hub.docker.com/r/wappalyzer/cli/)
* [Wappalyzer REST APIs](https://www.wappalyzer.com/api/)

## Documentation

Please read the [developer documentation](https://www.wappalyzer.com/docs).

## Quick start

```sh
git clone https://github.com/aliasio/wappalyzer
cd wappalyzer
yarn install
yarn run link
```

## Usage

### Command line

```sh
node src/drivers/npm/cli.js https://example.com
```

### Chrome extension

* Go go `about:extensions`
* Enable 'Developer mode'
* Click 'Load unpacked'
* Select `src/drivers/webextension`

### Firefox extension

* Go go `about:debugging#/runtime/this-firefox`
* Click 'Load Temporary Add-on'
* Select `src/drivers/webextension/manifest.json`

## Local build

To install a locally built version of the extension:
1/ build the extension
```sh
npm run build
```
2/ Make sure your browser accepts non-signed extensions.
  * Firefox: open `about:config` and set `xpinstall.signatures.required` to `false`
3/ Install the extension
  * Firefox: open `about:addons`, click on the cog and select `Install an extension from a file...`, select `./build/webextension.zip`
