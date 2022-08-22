# OpenLayers + Skypack

This example demonstrates how the `ol` package can be used with [Skypack](https://www.skypack.dev/).

Skypack allows web pages to import remote packages using ES modules without a development server or bundler.  When using Skypack, instead of importing directly from the `ol` package, you rewrite your imports to use URLs like `https://cdn.skypack.dev/ol`.  For example:

```js
import Map from 'https://cdn.skypack.dev/ol/Map.js';
```

See the `main.js` for a complete example.

Although you do not need a development server to bundle modules, using Skypack does require that you use HTTP(S) to view your `index.html` page.  So an HTTP server like Apache or nginx is required.

For developing locally, you can also launch a simple HTTP server using your favorite environment right from this directory:

    npx serve .                  # Node.js, or
    python3 -m http.server 3000  # Python, or
    php -S localhost:3000        # PHP, or
    ruby -run -e httpd . -p 3000 # Ruby

You should now be able to load the `index.html` map example at http://localhost:3000.
