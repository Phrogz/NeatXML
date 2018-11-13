# NeatXML
NeatXML is XML serialization (in JavaScript) with a few handy features.

The NeatXML module exports a single function, which takes an [XML Document](https://www.w3.org/TR/dom/#xml-document) or [Element](https://www.w3.org/TR/dom/#element) object to turn into a string, and an optional object specifying serialization options.

```js
import NeatXML from './neatxml.js';
const xmlString = NeatXML(xmlNodeOrDoc, options);
```

The `options` object accepts the following keys and values:

* `indent`: if set to a number or string, each node in the supplied hierarchy will be placed on its own line and indented by the number of spaces (if a number) or by repetitions of the string specified by this option.
* `strip`:  if set to `true`, remove leading/trailing whitespace from text nodes, and ignore whitespace-only nodes altogether.
* `sort`:   if set to `true`, sort attributes within elements based on their name, with attributes with no namespace appear before those with a prefix.
* `omitNS`: if set to a namespace URI string, or array of URIs, all attributes, elements, and namespace declarations matching the URI(s) will be omitted from the output. 
* `cdata`:  if set to `true`, all text nodes will be output as CDATA sections; if set to `false`, all CDATA nodes will be output as plain text.

When using the `indent` option you will likely also want to use the `strip` option.

## License & Contact

NeatXML is copyright ©2018 by Gavin Kistner and is released under
the [MIT License](http://www.opensource.org/licenses/mit-license.php).
See the LICENSE.txt file for more details.

For bugs or feature requests please open [issues on GitHub](https://github.com/Phrogz/NeatXML/issues).
For other communication you can [email the author directly](mailto:!@phrogz.net?subject=NeatXML).

## TODO (aka Known Limitations)

* Set up a robust test suite.
* Provide options for wrapping to set column widths.
* Provide options for formatting numeric attributes to a number of decimals.

## HISTORY

* **v0.9** — Initial release