<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [puppeteer](./puppeteer.md) &gt; [Puppeteer](./puppeteer.puppeteer.md) &gt; [networkConditions](./puppeteer.puppeteer.networkconditions.md)

## Puppeteer.networkConditions property

<b>Signature:</b>

```typescript
get networkConditions(): PredefinedNetworkConditions;
```

## Remarks

Returns a list of network conditions to be used with `page.emulateNetworkConditions(networkConditions)`. Actual list of predefined conditions can be found in [src/common/NetworkConditions.ts](https://github.com/puppeteer/puppeteer/blob/main/src/common/NetworkConditions.ts).

## Example


```js
const puppeteer = require('puppeteer');
const slow3G = puppeteer.networkConditions['Slow 3G'];

(async () => {
  const browser = await puppeteer.launch();
  const page = await browser.newPage();
  await page.emulateNetworkConditions(slow3G);
  await page.goto('https://www.google.com');
  // other actions...
  await browser.close();
})();

```

