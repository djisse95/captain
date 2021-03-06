<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [puppeteer](./puppeteer.md) &gt; [Browser](./puppeteer.browser.md) &gt; [createIncognitoBrowserContext](./puppeteer.browser.createincognitobrowsercontext.md)

## Browser.createIncognitoBrowserContext() method

Creates a new incognito browser context. This won't share cookies/cache with other browser contexts.

<b>Signature:</b>

```typescript
createIncognitoBrowserContext(): Promise<BrowserContext>;
```
<b>Returns:</b>

Promise&lt;[BrowserContext](./puppeteer.browsercontext.md)&gt;

## Example


```js
(async () => {
 const browser = await puppeteer.launch();
  // Create a new incognito browser context.
  const context = await browser.createIncognitoBrowserContext();
  // Create a new page in a pristine context.
  const page = await context.newPage();
  // Do stuff
  await page.goto('https://example.com');
})();

```

