# tabletop-element

An element allowing the easy use of Google Sheets in your projects.

## API

Example:
```
  <tabletop-element
    key="1dJbeUUovS3s2tNoJnS7BDoMRBIzfnHPJc3_NZoNJObA" <!-- key of the sheet -->
    simple-sheet="true" <!-- Whether to use "simpleSheet" mode -->
    wanted="latest" <!-- Which sheet to grab -->
    response="{{dataBoundVariable}}" <!-- Bind to a variable! -->
    on-response="_privateResponseHandler" <!-- Or handle response via event -->
  ></tabletop-element>

  <template is="dom-if" items="[[dataBoundVariable]]">
    <h1>[[item.label]]</h1>
  </template>
```

For full API details, please see [full online documentation](http://aendrew.com/tabletop-element/).

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install


## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    polyserve

Once running, you can preview your element at
`http://localhost:8080/components/tabletop-element/`, where `tabletop-element` is the name of the directory containing it.


## Testing Your Element

Simply navigate to the `/test` directory of your element to run its tests. If
you are using Polyserve: `http://localhost:8080/components/tabletop-element/test/`

### web-component-tester

The tests are compatible with [web-component-tester](https://github.com/Polymer/web-component-tester).
Install it via:

    npm install -g web-component-tester

Then, you can run your tests on _all_ of your local browsers via:

    wct

#### WCT Tips

`wct -l chrome` will only run tests in chrome.

`wct -p` will keep the browsers alive after test runs (refresh to re-run).

`wct test/some-file.html` will test only the files you specify.


## Changelog

- 0.2.0
  Removes service worker support; this should be handled on the app-level.

- 0.1.0
  Adds service worker support

- 0.0.1
  Initial release
