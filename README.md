# api documentation for  [bs-html-injector (v3.0.3)](https://github.com/shakyshane/html-injector#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-bs-html-injector.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-bs-html-injector) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-bs-html-injector.svg)](https://travis-ci.org/npmdoc/node-npmdoc-bs-html-injector)
#### Inject only HTML that has changed.

[![NPM](https://nodei.co/npm/bs-html-injector.png?downloads=true)](https://www.npmjs.com/package/bs-html-injector)

[![apidoc](https://npmdoc.github.io/node-npmdoc-bs-html-injector/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-bs-html-injector_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-bs-html-injector/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-bs-html-injector/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-bs-html-injector/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": "",
    "browser-sync:ui": {
        "hooks": {
            "markup": "ui/html-injector.html",
            "templates": [
                "ui/html-injector.directive.html"
            ],
            "client:js": [
                "ui/client.js"
            ]
        }
    },
    "bugs": {
        "url": "https://github.com/shakyshane/html-injector/issues"
    },
    "dependencies": {
        "debug": "^2.1.3",
        "dom-compare-temp": "^0.1.0",
        "jsdom": "^6.5.1",
        "request": "^2.40.0"
    },
    "description": "Inject only HTML that has changed.",
    "devDependencies": {
        "browser-sync": "2.12.12",
        "chai": "^3.3.0",
        "lodash-cli": "4.13.1",
        "mocha": "^2.3.3",
        "multiline": "^1.0.2",
        "socket.io-client": "^1.1.0"
    },
    "directories": {},
    "dist": {
        "shasum": "fb3a02f84488c7611842443f6d0cce145fe5b982",
        "tarball": "https://registry.npmjs.org/bs-html-injector/-/bs-html-injector-3.0.3.tgz"
    },
    "files": [
        "lib",
        "lodash.custom.js",
        "ui",
        "index.js",
        "client.js"
    ],
    "gitHead": "3ccc95eb6eee0b2bac4016613780e0b5226f03a1",
    "homepage": "https://github.com/shakyshane/html-injector#readme",
    "keywords": [
        "browser sync plugin",
        "html injection"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "shakyshane",
            "email": "shakyshane@gmail.com"
        }
    ],
    "name": "bs-html-injector",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/shakyshane/html-injector.git"
    },
    "scripts": {
        "lodash": "lodash include=isUndefined,isString,isArray,filter,assign,includes,uniqBy,uniq,without exports=node",
        "test": "mocha --reporter spec"
    },
    "version": "3.0.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module bs-html-injector](#apidoc.module.bs-html-injector)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.</span>html_injector (opts)](#apidoc.element.bs-html-injector.html_injector)
1.  function <span class="apidocSignatureSpan">bs-html-injector.</span>lodash_custom
1.  [function <span class="apidocSignatureSpan">bs-html-injector.</span>plugin (opts, bs)](#apidoc.element.bs-html-injector.plugin)
1.  object <span class="apidocSignatureSpan">bs-html-injector.</span>hooks
1.  object <span class="apidocSignatureSpan">bs-html-injector.</span>html_injector.prototype
1.  object <span class="apidocSignatureSpan">bs-html-injector.</span>injector
1.  object <span class="apidocSignatureSpan">bs-html-injector.</span>utils

#### [module bs-html-injector.html_injector](#apidoc.module.bs-html-injector.html_injector)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.</span>html_injector (opts)](#apidoc.element.bs-html-injector.html_injector.html_injector)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.html_injector.</span>getDiffs (item1, item2, opts)](#apidoc.element.bs-html-injector.html_injector.getDiffs)

#### [module bs-html-injector.html_injector.prototype](#apidoc.module.bs-html-injector.html_injector.prototype)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.html_injector.prototype.</span>getDiffs (item1, item2, opts)](#apidoc.element.bs-html-injector.html_injector.prototype.getDiffs)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.html_injector.prototype.</span>getTasks (parent, diffs, restrictions, currentUrl)](#apidoc.element.bs-html-injector.html_injector.prototype.getTasks)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.html_injector.prototype.</span>process (item1, item2, url, opts)](#apidoc.element.bs-html-injector.html_injector.prototype.process)

#### [module bs-html-injector.injector](#apidoc.module.bs-html-injector.injector)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.injector.</span>compareDoms (oldDom, newDom, opts)](#apidoc.element.bs-html-injector.injector.compareDoms)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.injector.</span>createDom (string)](#apidoc.element.bs-html-injector.injector.createDom)

#### [module bs-html-injector.lodash_custom](#apidoc.module.bs-html-injector.lodash_custom)
1.  function <span class="apidocSignatureSpan">bs-html-injector.</span>lodash_custom
1.  function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>_
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>assign ()](#apidoc.element.bs-html-injector.lodash_custom.assign)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>eq (value, other)](#apidoc.element.bs-html-injector.lodash_custom.eq)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>filter (collection, predicate)](#apidoc.element.bs-html-injector.lodash_custom.filter)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>get (object, path, defaultValue)](#apidoc.element.bs-html-injector.lodash_custom.get)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>hasIn (object, path)](#apidoc.element.bs-html-injector.lodash_custom.hasIn)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>identity (value)](#apidoc.element.bs-html-injector.lodash_custom.identity)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>includes (collection, value, fromIndex, guard)](#apidoc.element.bs-html-injector.lodash_custom.includes)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isArguments (value)](#apidoc.element.bs-html-injector.lodash_custom.isArguments)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isArray ()](#apidoc.element.bs-html-injector.lodash_custom.isArray)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isArrayLike (value)](#apidoc.element.bs-html-injector.lodash_custom.isArrayLike)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isArrayLikeObject (value)](#apidoc.element.bs-html-injector.lodash_custom.isArrayLikeObject)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isBuffer (value)](#apidoc.element.bs-html-injector.lodash_custom.isBuffer)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isFunction (value)](#apidoc.element.bs-html-injector.lodash_custom.isFunction)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isLength (value)](#apidoc.element.bs-html-injector.lodash_custom.isLength)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isObject (value)](#apidoc.element.bs-html-injector.lodash_custom.isObject)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isObjectLike (value)](#apidoc.element.bs-html-injector.lodash_custom.isObjectLike)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isString (value)](#apidoc.element.bs-html-injector.lodash_custom.isString)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isSymbol (value)](#apidoc.element.bs-html-injector.lodash_custom.isSymbol)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isTypedArray (value)](#apidoc.element.bs-html-injector.lodash_custom.isTypedArray)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isUndefined (value)](#apidoc.element.bs-html-injector.lodash_custom.isUndefined)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>iteratee (func)](#apidoc.element.bs-html-injector.lodash_custom.iteratee)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>keys (object)](#apidoc.element.bs-html-injector.lodash_custom.keys)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>memoize (func, resolver)](#apidoc.element.bs-html-injector.lodash_custom.memoize)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>noop ()](#apidoc.element.bs-html-injector.lodash_custom.noop)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>property (path)](#apidoc.element.bs-html-injector.lodash_custom.property)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>rest (func, start)](#apidoc.element.bs-html-injector.lodash_custom.rest)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>stubArray ()](#apidoc.element.bs-html-injector.lodash_custom.stubArray)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>stubFalse ()](#apidoc.element.bs-html-injector.lodash_custom.stubFalse)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>toFinite (value)](#apidoc.element.bs-html-injector.lodash_custom.toFinite)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>toInteger (value)](#apidoc.element.bs-html-injector.lodash_custom.toInteger)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>toNumber (value)](#apidoc.element.bs-html-injector.lodash_custom.toNumber)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>toString (value)](#apidoc.element.bs-html-injector.lodash_custom.toString)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>uniq (array)](#apidoc.element.bs-html-injector.lodash_custom.uniq)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>uniqBy (array, iteratee)](#apidoc.element.bs-html-injector.lodash_custom.uniqBy)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>values (object)](#apidoc.element.bs-html-injector.lodash_custom.values)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>without ()](#apidoc.element.bs-html-injector.lodash_custom.without)
1.  string <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>VERSION

#### [module bs-html-injector.utils](#apidoc.module.bs-html-injector.utils)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.utils.</span>removeDupes (differences)](#apidoc.element.bs-html-injector.utils.removeDupes)
1.  [function <span class="apidocSignatureSpan">bs-html-injector.utils.</span>removeExcluded (diffs, excludeList)](#apidoc.element.bs-html-injector.utils.removeExcluded)



# <a name="apidoc.module.bs-html-injector"></a>[module bs-html-injector](#apidoc.module.bs-html-injector)

#### <a name="apidoc.element.bs-html-injector.html_injector"></a>[function <span class="apidocSignatureSpan">bs-html-injector.</span>html_injector (opts)](#apidoc.element.bs-html-injector.html_injector)
- description and source-code
```javascript
html_injector = function (opts) {

    var html = this;

    if (!(html instanceof HtmlInjector)) {
        return new HtmlInjector(opts);
    }

    html.opts = _.assign({}, defaults, opts);
    html.cache = {};
    html.emitCount = 0;

    if (_.isUndefined(html.opts.enabled)) {
        html.opts.enabled = true;
    }

<span class="apidocCodeCommentSpan">    /**
     * @returns {Number}
     */
</span>    html.hasCached = function () {
        return Object.keys(html.cache).length;
    };

    return html;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bs-html-injector.plugin"></a>[function <span class="apidocSignatureSpan">bs-html-injector.</span>plugin (opts, bs)](#apidoc.element.bs-html-injector.plugin)
- description and source-code
```javascript
plugin = function (opts, bs) {

    opts = opts || {};

    var logger       = bs.getLogger(config.PLUGIN_NAME).info("Running...");

    if (typeof opts.logLevel !== "undefined") {
        logger.setLevel(opts.logLevel);
    }

    var htmlInjector = instance = new HtmlInjector(opts, logger, bs);
    var opts         = htmlInjector.opts;
    var clients      = bs.io.of(bs.options.getIn(["socket", "namespace"]));

    if (bs.ui) {
        addUiEvents();
    }

<span class="apidocCodeCommentSpan">    /**
     * Add UI events if running
     */
</span>    function addUiEvents () {

        var ui = bs.io.of(bs.ui.config.getIn(["socket", "namespace"]));

        bs.ui.listen(config.PLUGIN_NAME, {
            "restriction:add": function (data) {
                opts.restrictions = _.uniq(opts.restrictions.concat([data]));
                updateOptions(opts);
            },
            "restriction:remove": function (data) {
                opts.restrictions = _.without(opts.restrictions, data);
                updateOptions(opts);
            }
        });

        function updateOptions (opts) {
            bs.events.emit("plugins:opts", {
                name: config.PLUGIN_NAME,
                opts: opts
            });
            ui.emit("options:update", {
                name: config.PLUGIN_NAME,
                opts: bs.getUserPlugin(config.PLUGIN_NAME).opts
            });
        }
    }

    enabled = htmlInjector.opts.enabled;

    /**
     * Configure event
     */
    bs.events.on("plugins:configure", function (data) {

        if (data.name !== config.PLUGIN_NAME) {
            return;
        }

        var msg = "{cyan:Enabled";

        if (!data.active) {
            msg = "{yellow:Disabled";
        } else {
            clients.emit("browser:reload");
        }

        logger.info(msg);

        enabled = data.active;
    });

    /**
     * File changed event
     */
    bs.events.on("file:changed", fileChangedEvent);

    /**
     * Internal event
     */
    emitter.on(config.PLUGIN_EVENT, pluginEvent);

    /**
     * Socket Connection event
     */
    clients.on("connection", handleSocketConnection);

    /**
     * Catch the above ^
     */
    function handleSocketConnection (client) {
        client.on("client:url", handleUrlEvent);
    }

    function getRequestOptions(url) {
        return {
            url: url,
            headers: {
                "Accept": "text/html"
            }
        }
    }

    /**
     * @param data
     */
    function handleUrlEvent (data) {

        if (!enabled) {

            return;
        }

        request(getRequestOptions(data.url), function (error, response, body) {

            logger.debug("Stashing: {magenta:%s", data.url);

            if (!error && response.statusCode == 200) {
                htmlInjector.cache[data.url] = createDom(body);
            }
        });
    }

    function fileChangedEvent (data) {

        if (!_.isUndefined(data.event) && data.event !== "change") {
            return;
        }

        if (!enabled) {

            if (opts.handoff && data._origin !== config.PLUGIN_NAME) {
                data.namespace = "core";
                data._origin = config.PLUGIN_NAME;
                bs.events.emit("file:changed", data);
            }

            return;
        }

        if (data.namespace !== config.PLUGIN_NAME) {
            debug('Ignoring file change to ', data.path);
            return;
        }

        debug('Responding to file change event', data.namespace);

        requestNew(opts);
    }

    function pluginEvent () {

        if (!htmlInjector.hasCached()) {
            return;
        }

        doNewRequest();
    }

    function doNewRequest() {

        if (!enabled || !htmlInjector.hasCached()) {
            return;
        }

        logger.debug("Getting new HTML from: {magenta:%s} urls", Object.keys(htmlInjector.cache).length);

        requestNew(opts);
    }
    /**
     * Request new version of Dom
     * @param {String} url
     * @param {Object} opts - plugin options
     */
    function requestNew (opts) {

        // Remove any
        var ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.bs-html-injector.html_injector"></a>[module bs-html-injector.html_injector](#apidoc.module.bs-html-injector.html_injector)

#### <a name="apidoc.element.bs-html-injector.html_injector.html_injector"></a>[function <span class="apidocSignatureSpan">bs-html-injector.</span>html_injector (opts)](#apidoc.element.bs-html-injector.html_injector.html_injector)
- description and source-code
```javascript
html_injector = function (opts) {

    var html = this;

    if (!(html instanceof HtmlInjector)) {
        return new HtmlInjector(opts);
    }

    html.opts = _.assign({}, defaults, opts);
    html.cache = {};
    html.emitCount = 0;

    if (_.isUndefined(html.opts.enabled)) {
        html.opts.enabled = true;
    }

<span class="apidocCodeCommentSpan">    /**
     * @returns {Number}
     */
</span>    html.hasCached = function () {
        return Object.keys(html.cache).length;
    };

    return html;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bs-html-injector.html_injector.getDiffs"></a>[function <span class="apidocSignatureSpan">bs-html-injector.html_injector.</span>getDiffs (item1, item2, opts)](#apidoc.element.bs-html-injector.html_injector.getDiffs)
- description and source-code
```javascript
getDiffs = function (item1, item2, opts) {
<span class="apidocCodeCommentSpan">    /**
     * @param newDom
     * @param item2
     * @param [opts]
     * @returns {*}
     */
</span>
    opts = opts || {};

    if (_.isString(item2)) {
        item2 = createDom(item2);
    }

    var newDom  = createDom(item1);
    var results = compareDoms(item2, newDom, opts);

    if (results.length) {
        results = results.map(function (result) {
            result.diffs = utils.removeDupes(result.diffs);
            result.diffs = utils.removeExcluded(result.diffs, opts.excludedTags);
            return result;
        });
    }

    return results;
}
```
- example usage
```shell
...
 * @param item2
 * @param url
 * @param opts
 */
HtmlInjector.prototype.process = function (item1, item2, url, opts) {

var html    = this;
var results = html.getDiffs(item1, item2, opts);
var out     = [];

if (results.length) {
    results.forEach(function (result) {
        out = out.concat(html.getTasks(result.parent, result.diffs, result.restriction, url));
    });
    html.cache[url] = createDom(item1);
...
```



# <a name="apidoc.module.bs-html-injector.html_injector.prototype"></a>[module bs-html-injector.html_injector.prototype](#apidoc.module.bs-html-injector.html_injector.prototype)

#### <a name="apidoc.element.bs-html-injector.html_injector.prototype.getDiffs"></a>[function <span class="apidocSignatureSpan">bs-html-injector.html_injector.prototype.</span>getDiffs (item1, item2, opts)](#apidoc.element.bs-html-injector.html_injector.prototype.getDiffs)
- description and source-code
```javascript
getDiffs = function (item1, item2, opts) {
<span class="apidocCodeCommentSpan">    /**
     * @param newDom
     * @param item2
     * @param [opts]
     * @returns {*}
     */
</span>
    opts = opts || {};

    if (_.isString(item2)) {
        item2 = createDom(item2);
    }

    var newDom  = createDom(item1);
    var results = compareDoms(item2, newDom, opts);

    if (results.length) {
        results = results.map(function (result) {
            result.diffs = utils.removeDupes(result.diffs);
            result.diffs = utils.removeExcluded(result.diffs, opts.excludedTags);
            return result;
        });
    }

    return results;
}
```
- example usage
```shell
...
 * @param item2
 * @param url
 * @param opts
 */
HtmlInjector.prototype.process = function (item1, item2, url, opts) {

var html    = this;
var results = html.getDiffs(item1, item2, opts);
var out     = [];

if (results.length) {
    results.forEach(function (result) {
        out = out.concat(html.getTasks(result.parent, result.diffs, result.restriction, url));
    });
    html.cache[url] = createDom(item1);
...
```

#### <a name="apidoc.element.bs-html-injector.html_injector.prototype.getTasks"></a>[function <span class="apidocSignatureSpan">bs-html-injector.html_injector.prototype.</span>getTasks (parent, diffs, restrictions, currentUrl)](#apidoc.element.bs-html-injector.html_injector.prototype.getTasks)
- description and source-code
```javascript
getTasks = function (parent, diffs, restrictions, currentUrl) {

    var tasks = [];

    diffs.forEach(function (item) {

        item.diff.type = item.diff.type || "node";

        var element = getElement(parent, item);

        if (element && element.domNode) {

            if (item.diff.type) {

                var obj = {
                    tagName:  item.tagName,
                    index:    item.index,
                    cssText:  element.domNode.style.cssText,
                    attrs:    element.attrs,
                    diff:     item.diff,
                    url:      currentUrl,
                    restrictions: restrictions
                };

                switch (item.diff.type) {

                    case 'attribute':
                        // no-op, use default obj
                        break;

                    default:
                        obj.html = element.domNode.innerHTML;
                        break;
                }

                tasks.push(obj);
            }
        }
    });

    if (tasks.length) {
        return tasks;
    }

    return [];
}
```
- example usage
```shell
...

    var html    = this;
    var results = html.getDiffs(item1, item2, opts);
    var out     = [];

    if (results.length) {
        results.forEach(function (result) {
            out = out.concat(html.getTasks(result.parent, result.diffs, result.restriction, url));
        });
        html.cache[url] = createDom(item1);
    }

    return out;
};
...
```

#### <a name="apidoc.element.bs-html-injector.html_injector.prototype.process"></a>[function <span class="apidocSignatureSpan">bs-html-injector.html_injector.prototype.</span>process (item1, item2, url, opts)](#apidoc.element.bs-html-injector.html_injector.prototype.process)
- description and source-code
```javascript
process = function (item1, item2, url, opts) {

    var html    = this;
    var results = html.getDiffs(item1, item2, opts);
    var out     = [];

    if (results.length) {
        results.forEach(function (result) {
            out = out.concat(html.getTasks(result.parent, result.diffs, result.restriction, url));
        });
        html.cache[url] = createDom(item1);
    }

    return out;
}
```
- example usage
```shell
...

            debug("requesting %s", url);

            request(getRequestOptions(url), function (error, response, body) {

                if (!error && response.statusCode == 200) {

var tasks = htmlInjector.process(body, htmlInjector.cache[url], url, opts);

if (tasks.length) {
    debug("%s tasks returned", tasks.length);
    tasks.forEach(function (task) {
        debug("Task: TAG: %s, INDEX: %s", task.tagName, task.index);
        clients.emit(config.CLIENT_EVENT, task);
    });
...
```



# <a name="apidoc.module.bs-html-injector.injector"></a>[module bs-html-injector.injector](#apidoc.module.bs-html-injector.injector)

#### <a name="apidoc.element.bs-html-injector.injector.compareDoms"></a>[function <span class="apidocSignatureSpan">bs-html-injector.injector.</span>compareDoms (oldDom, newDom, opts)](#apidoc.element.bs-html-injector.injector.compareDoms)
- description and source-code
```javascript
function compareDoms(oldDom, newDom, opts) {

    opts = opts || {};
    opts.restrictions = opts.restrictions || [];

    var diffs = [];

    if (!oldDom || !newDom) {
        return diffs;
    }

    if (opts.restrictions.length) {
        opts.restrictions.forEach(function (restriction) {
            getResults(restriction);
        });
    } else {
        getResults("html");
    }

    function getResults (restriction) {
        var dom1, dom2, node;

        if (restriction !== "html") {
            var match1 = oldDom.querySelectorAll(restriction);
            var match2 = newDom.querySelectorAll(restriction);
            if (match1.length && match2.length) {

                dom1 = createDom(match1[0].innerHTML);
                dom2 = createDom(match2[0].innerHTML);
            } else {
                debug("Selector %s not found", restriction);
            }
        } else {
            dom1 = oldDom;
            dom2 = newDom;
        }

        if (!dom1 || !dom2) {
            debug("2 doms not found");
            return;
        }

        var result = compare(dom1, dom2, {
            formatFailure: function (failure, domNode) {
                node = domNode;
                var allElems    = domNode.ownerDocument.getElementsByTagName(domNode.nodeName);
                failure.index   = Array.prototype.indexOf.call(allElems, domNode);
                failure.tagName = domNode.nodeName;
                return failure;
            }
        });

        var same = result.getResult(); // false cause' trees are different

        if (!same) {
            diffs.push({
                restriction: restriction,
                diffs:    result.getDifferences(),
                parent:   dom2
            });
        }
    }

    return diffs;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bs-html-injector.injector.createDom"></a>[function <span class="apidocSignatureSpan">bs-html-injector.injector.</span>createDom (string)](#apidoc.element.bs-html-injector.injector.createDom)
- description and source-code
```javascript
function createDom(string) {
    return jsdom(string);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.bs-html-injector.lodash_custom"></a>[module bs-html-injector.lodash_custom](#apidoc.module.bs-html-injector.lodash_custom)

#### <a name="apidoc.element.bs-html-injector.lodash_custom.assign"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>assign ()](#apidoc.element.bs-html-injector.lodash_custom.assign)
- description and source-code
```javascript
assign = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      array = Array(length);

  while (++index < length) {
    array[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, array);
    case 1: return func.call(this, args[0], array);
    case 2: return func.call(this, args[0], args[1], array);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = array;
  return apply(func, this, otherArgs);
}
```
- example usage
```shell
...

var html = this;

if (!(html instanceof HtmlInjector)) {
    return new HtmlInjector(opts);
}

html.opts = _.assign({}, defaults, opts);
html.cache = {};
html.emitCount = 0;

if (_.isUndefined(html.opts.enabled)) {
    html.opts.enabled = true;
}
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.eq"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>eq (value, other)](#apidoc.element.bs-html-injector.lodash_custom.eq)
- description and source-code
```javascript
function eq(value, other) {
  return value === other || (value !== value && other !== other);
}
```
- example usage
```shell
...
* @param {*} other The other value to compare.
* @returns {boolean} Returns 'true' if the values are equivalent, else 'false'.
* @example
*
* var object = { 'user': 'fred' };
* var other = { 'user': 'fred' };
*
* _.eq(object, object);
* // => true
*
* _.eq(object, other);
* // => false
*
* _.eq('a', 'a');
* // => true
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.filter"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>filter (collection, predicate)](#apidoc.element.bs-html-injector.lodash_custom.filter)
- description and source-code
```javascript
function filter(collection, predicate) {
  var func = isArray(collection) ? arrayFilter : baseFilter;
  return func(collection, getIteratee(predicate, 3));
}
```
- example usage
```shell
...

   /**
    * @param diffs
    * @param excludeList
    * @returns {*}
    */
   removeExcluded: function (diffs, excludeList) {
       return _.filter(diffs, function (item) {
           return !_.includes(excludeList, item.tagName);
       });
   }
};

/**
* Not currently used... needs work.
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.get"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>get (object, path, defaultValue)](#apidoc.element.bs-html-injector.lodash_custom.get)
- description and source-code
```javascript
function get(object, path, defaultValue) {
  var result = object == null ? undefined : baseGet(object, path);
  return result === undefined ? defaultValue : result;
}
```
- example usage
```shell
...
 * @private
 * @name get
 * @memberOf MapCache
 * @param {string} key The key of the value to get.
 * @returns {*} Returns the entry value.
 */
function mapCacheGet(key) {
  return getMapData(this, key).get(key);
}

/**
 * Checks if a map value for 'key' exists.
 *
 * @private
 * @name has
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.hasIn"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>hasIn (object, path)](#apidoc.element.bs-html-injector.lodash_custom.hasIn)
- description and source-code
```javascript
function hasIn(object, path) {
  return object != null && hasPath(object, path, baseHasIn);
}
```
- example usage
```shell
...
* @param {Object} object The object to query.
* @param {Array|string} path The path to check.
* @returns {boolean} Returns 'true' if 'path' exists, else 'false'.
* @example
*
* var object = _.create({ 'a': _.create({ 'b': 2 }) });
*
* _.hasIn(object, 'a');
* // => true
*
* _.hasIn(object, 'a.b');
* // => true
*
* _.hasIn(object, ['a', 'b']);
* // => true
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.identity"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>identity (value)](#apidoc.element.bs-html-injector.lodash_custom.identity)
- description and source-code
```javascript
function identity(value) {
  return value;
}
```
- example usage
```shell
...
 * @category Util
 * @param {*} value Any value.
 * @returns {*} Returns 'value'.
 * @example
 *
 * var object = { 'user': 'fred' };
 *
 * console.log(_.identity(object) === object);
 * // => true
 */
function identity(value) {
  return value;
}

/**
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.includes"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>includes (collection, value, fromIndex, guard)](#apidoc.element.bs-html-injector.lodash_custom.includes)
- description and source-code
```javascript
function includes(collection, value, fromIndex, guard) {
  collection = isArrayLike(collection) ? collection : values(collection);
  fromIndex = (fromIndex && !guard) ? toInteger(fromIndex) : 0;

  var length = collection.length;
  if (fromIndex < 0) {
    fromIndex = nativeMax(length + fromIndex, 0);
  }
  return isString(collection)
    ? (fromIndex <= length && collection.indexOf(value, fromIndex) > -1)
    : (!!length && baseIndexOf(collection, value, fromIndex) > -1);
}
```
- example usage
```shell
...
   /**
    * @param diffs
    * @param excludeList
    * @returns {*}
    */
   removeExcluded: function (diffs, excludeList) {
       return _.filter(diffs, function (item) {
           return !_.includes(excludeList, item.tagName);
       });
   }
};

/**
* Not currently used... needs work.
* @param {Array} differences
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.isArguments"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isArguments (value)](#apidoc.element.bs-html-injector.lodash_custom.isArguments)
- description and source-code
```javascript
function isArguments(value) {
  // Safari 8.1 incorrectly makes 'arguments.callee' enumerable in strict mode.
  return isArrayLikeObject(value) && hasOwnProperty.call(value, 'callee') &&
    (!propertyIsEnumerable.call(value, 'callee') || objectToString.call(value) == argsTag);
}
```
- example usage
```shell
...
 * @since 0.1.0
 * @category Lang
 * @param {*} value The value to check.
 * @returns {boolean} Returns 'true' if 'value' is correctly classified,
 *  else 'false'.
 * @example
 *
 * _.isArguments(function() { return arguments; }());
 * // => true
 *
 * _.isArguments([1, 2, 3]);
 * // => false
 */
function isArguments(value) {
  // Safari 8.1 incorrectly makes 'arguments.callee' enumerable in strict mode.
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.isArray"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isArray ()](#apidoc.element.bs-html-injector.lodash_custom.isArray)
- description and source-code
```javascript
function isArray() { [native code] }
```
- example usage
```shell
...
 * // Returns an unwrapped value.
 * wrapped.reduce(_.add);
 * // => 6
 *
 * // Returns a wrapped value.
 * var squares = wrapped.map(square);
 *
 * _.isArray(squares);
 * // => false
 *
 * _.isArray(squares.value());
 * // => true
 */
function lodash() {
  // No operation performed.
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.isArrayLike"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isArrayLike (value)](#apidoc.element.bs-html-injector.lodash_custom.isArrayLike)
- description and source-code
```javascript
function isArrayLike(value) {
  return value != null && isLength(getLength(value)) && !isFunction(value);
}
```
- example usage
```shell
...
* @memberOf _
* @since 4.0.0
* @category Lang
* @param {*} value The value to check.
* @returns {boolean} Returns 'true' if 'value' is array-like, else 'false'.
* @example
*
* _.isArrayLike([1, 2, 3]);
* // => true
*
* _.isArrayLike(document.body.children);
* // => true
*
* _.isArrayLike('abc');
* // => true
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.isArrayLikeObject"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isArrayLikeObject (value)](#apidoc.element.bs-html-injector.lodash_custom.isArrayLikeObject)
- description and source-code
```javascript
function isArrayLikeObject(value) {
  return isObjectLike(value) && isArrayLike(value);
}
```
- example usage
```shell
...
* @since 4.0.0
* @category Lang
* @param {*} value The value to check.
* @returns {boolean} Returns 'true' if 'value' is an array-like object,
*  else 'false'.
* @example
*
* _.isArrayLikeObject([1, 2, 3]);
* // => true
*
* _.isArrayLikeObject(document.body.children);
* // => true
*
* _.isArrayLikeObject('abc');
* // => false
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.isBuffer"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isBuffer (value)](#apidoc.element.bs-html-injector.lodash_custom.isBuffer)
- description and source-code
```javascript
isBuffer = function (value) {
  return value instanceof Buffer;
}
```
- example usage
```shell
...
 * @memberOf _
 * @since 4.3.0
 * @category Lang
 * @param {*} value The value to check.
 * @returns {boolean} Returns 'true' if 'value' is a buffer, else 'false'.
 * @example
 *
 * _.isBuffer(new Buffer(2));
 * // => true
 *
 * _.isBuffer(new Uint8Array(2));
 * // => false
 */
var isBuffer = !Buffer ? stubFalse : function(value) {
  return value instanceof Buffer;
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.isFunction"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isFunction (value)](#apidoc.element.bs-html-injector.lodash_custom.isFunction)
- description and source-code
```javascript
function isFunction(value) {
  // The use of 'Object#toString' avoids issues with the 'typeof' operator
  // in Safari 8 which returns 'object' for typed array and weak map constructors,
  // and PhantomJS 1.9 which returns 'function' for 'NodeList' instances.
  var tag = isObject(value) ? objectToString.call(value) : '';
  return tag == funcTag || tag == genTag;
}
```
- example usage
```shell
...
 * @since 0.1.0
 * @category Lang
 * @param {*} value The value to check.
 * @returns {boolean} Returns 'true' if 'value' is correctly classified,
 *  else 'false'.
 * @example
 *
 * _.isFunction(_);
 * // => true
 *
 * _.isFunction(/abc/);
 * // => false
 */
function isFunction(value) {
  // The use of 'Object#toString' avoids issues with the 'typeof' operator
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.isLength"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isLength (value)](#apidoc.element.bs-html-injector.lodash_custom.isLength)
- description and source-code
```javascript
function isLength(value) {
  return typeof value == 'number' &&
    value > -1 && value % 1 == 0 && value <= MAX_SAFE_INTEGER;
}
```
- example usage
```shell
...
* @since 4.0.0
* @category Lang
* @param {*} value The value to check.
* @returns {boolean} Returns 'true' if 'value' is a valid length,
*  else 'false'.
* @example
*
* _.isLength(3);
* // => true
*
* _.isLength(Number.MIN_VALUE);
* // => false
*
* _.isLength(Infinity);
* // => false
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.isObject"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isObject (value)](#apidoc.element.bs-html-injector.lodash_custom.isObject)
- description and source-code
```javascript
function isObject(value) {
  var type = typeof value;
  return !!value && (type == 'object' || type == 'function');
}
```
- example usage
```shell
...
* @memberOf _
* @since 0.1.0
* @category Lang
* @param {*} value The value to check.
* @returns {boolean} Returns 'true' if 'value' is an object, else 'false'.
* @example
*
* _.isObject({});
* // => true
*
* _.isObject([1, 2, 3]);
* // => true
*
* _.isObject(_.noop);
* // => true
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.isObjectLike"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isObjectLike (value)](#apidoc.element.bs-html-injector.lodash_custom.isObjectLike)
- description and source-code
```javascript
function isObjectLike(value) {
  return !!value && typeof value == 'object';
}
```
- example usage
```shell
...
* @memberOf _
* @since 4.0.0
* @category Lang
* @param {*} value The value to check.
* @returns {boolean} Returns 'true' if 'value' is object-like, else 'false'.
* @example
*
* _.isObjectLike({});
* // => true
*
* _.isObjectLike([1, 2, 3]);
* // => true
*
* _.isObjectLike(_.noop);
* // => false
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.isString"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isString (value)](#apidoc.element.bs-html-injector.lodash_custom.isString)
- description and source-code
```javascript
function isString(value) {
  return typeof value == 'string' ||
    (!isArray(value) && isObjectLike(value) && objectToString.call(value) == stringTag);
}
```
- example usage
```shell
...
 * @param item2
 * @param [opts]
 * @returns {*}
 */

opts = opts || {};

if (_.isString(item2)) {
    item2 = createDom(item2);
}

var newDom  = createDom(item1);
var results = compareDoms(item2, newDom, opts);

if (results.length) {
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.isSymbol"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isSymbol (value)](#apidoc.element.bs-html-injector.lodash_custom.isSymbol)
- description and source-code
```javascript
function isSymbol(value) {
  return typeof value == 'symbol' ||
    (isObjectLike(value) && objectToString.call(value) == symbolTag);
}
```
- example usage
```shell
...
 * @since 4.0.0
 * @category Lang
 * @param {*} value The value to check.
 * @returns {boolean} Returns 'true' if 'value' is correctly classified,
 *  else 'false'.
 * @example
 *
 * _.isSymbol(Symbol.iterator);
 * // => true
 *
 * _.isSymbol('abc');
 * // => false
 */
function isSymbol(value) {
  return typeof value == 'symbol' ||
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.isTypedArray"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isTypedArray (value)](#apidoc.element.bs-html-injector.lodash_custom.isTypedArray)
- description and source-code
```javascript
function isTypedArray(value) {
  return isObjectLike(value) &&
    isLength(value.length) && !!typedArrayTags[objectToString.call(value)];
}
```
- example usage
```shell
...
 * @since 3.0.0
 * @category Lang
 * @param {*} value The value to check.
 * @returns {boolean} Returns 'true' if 'value' is correctly classified,
 *  else 'false'.
 * @example
 *
 * _.isTypedArray(new Uint8Array);
 * // => true
 *
 * _.isTypedArray([]);
 * // => false
 */
function isTypedArray(value) {
  return isObjectLike(value) &&
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.isUndefined"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>isUndefined (value)](#apidoc.element.bs-html-injector.lodash_custom.isUndefined)
- description and source-code
```javascript
function isUndefined(value) {
  return value === undefined;
}
```
- example usage
```shell
...
    htmlInjector.cache[data.url] = createDom(body);
}
        });
    }

    function fileChangedEvent (data) {

        if (!_.isUndefined(data.event) && data.event !== "change") {
return;
        }

        if (!enabled) {

if (opts.handoff && data._origin !== config.PLUGIN_NAME) {
    data.namespace = "core";
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.iteratee"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>iteratee (func)](#apidoc.element.bs-html-injector.lodash_custom.iteratee)
- description and source-code
```javascript
function iteratee(func) {
  return baseIteratee(typeof func == 'function' ? func : baseClone(func, true));
}
```
- example usage
```shell
...
*
* var users = [
*   { 'user': 'barney', 'age': 36, 'active': true },
*   { 'user': 'fred',   'age': 40, 'active': false }
* ];
*
* // The '_.matches' iteratee shorthand.
* _.filter(users, _.iteratee({ 'user': 'barney', 'active': true }));
* // => [{ 'user': 'barney', 'age': 36, 'active': true }]
*
* // The '_.matchesProperty' iteratee shorthand.
* _.filter(users, _.iteratee(['user', 'fred']));
* // => [{ 'user': 'fred', 'age': 40 }]
*
* // The '_.property' iteratee shorthand.
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.keys"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>keys (object)](#apidoc.element.bs-html-injector.lodash_custom.keys)
- description and source-code
```javascript
function keys(object) {
  var isProto = isPrototype(object);
  if (!(isProto || isArrayLike(object))) {
    return baseKeys(object);
  }
  var indexes = indexKeys(object),
      skipIndexes = !!indexes,
      result = indexes || [],
      length = result.length;

  for (var key in object) {
    if (baseHas(object, key) &&
        !(skipIndexes && (key == 'length' || isIndex(key, length))) &&
        !(isProto && key == 'constructor')) {
      result.push(key);
    }
  }
  return result;
}
```
- example usage
```shell
...

function doNewRequest() {

    if (!enabled || !htmlInjector.hasCached()) {
        return;
    }

    logger.debug("Getting new HTML from: {magenta:%s} urls", Object.keys(htmlInjector.cache).length);

    requestNew(opts);
}
/**
 * Request new version of Dom
 * @param {String} url
 * @param {Object} opts - plugin options
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.memoize"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>memoize (func, resolver)](#apidoc.element.bs-html-injector.lodash_custom.memoize)
- description and source-code
```javascript
function memoize(func, resolver) {
  if (typeof func != 'function' || (resolver && typeof resolver != 'function')) {
    throw new TypeError(FUNC_ERROR_TEXT);
  }
  var memoized = function() {
    var args = arguments,
        key = resolver ? resolver.apply(this, args) : args[0],
        cache = memoized.cache;

    if (cache.has(key)) {
      return cache.get(key);
    }
    var result = func.apply(this, args);
    memoized.cache = cache.set(key, result);
    return result;
  };
  memoized.cache = new (memoize.Cache || MapCache);
  return memoized;
}
```
- example usage
```shell
...
* @param {Function} [resolver] The function to resolve the cache key.
* @returns {Function} Returns the new memoized function.
* @example
*
* var object = { 'a': 1, 'b': 2 };
* var other = { 'c': 3, 'd': 4 };
*
* var values = _.memoize(_.values);
* values(object);
* // => [1, 2]
*
* values(other);
* // => [3, 4]
*
* object.a = 2;
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.noop"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>noop ()](#apidoc.element.bs-html-injector.lodash_custom.noop)
- description and source-code
```javascript
function noop() {
  // No operation performed.
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.property"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>property (path)](#apidoc.element.bs-html-injector.lodash_custom.property)
- description and source-code
```javascript
function property(path) {
  return isKey(path) ? baseProperty(toKey(path)) : basePropertyDeep(path);
}
```
- example usage
```shell
...
 * @example
 *
 * var objects = [
 *   { 'a': { 'b': 2 } },
 *   { 'a': { 'b': 1 } }
 * ];
 *
 * _.map(objects, _.property('a.b'));
 * // => [2, 1]
 *
 * _.map(_.sortBy(objects, _.property(['a', 'b'])), 'a.b');
 * // => [1, 2]
 */
function property(path) {
  return isKey(path) ? baseProperty(toKey(path)) : basePropertyDeep(path);
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.rest"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>rest (func, start)](#apidoc.element.bs-html-injector.lodash_custom.rest)
- description and source-code
```javascript
function rest(func, start) {
  if (typeof func != 'function') {
    throw new TypeError(FUNC_ERROR_TEXT);
  }
  start = nativeMax(start === undefined ? (func.length - 1) : toInteger(start), 0);
  return function() {
    var args = arguments,
        index = -1,
        length = nativeMax(args.length - start, 0),
        array = Array(length);

    while (++index < length) {
      array[index] = args[start + index];
    }
    switch (start) {
      case 0: return func.call(this, array);
      case 1: return func.call(this, args[0], array);
      case 2: return func.call(this, args[0], args[1], array);
    }
    var otherArgs = Array(start + 1);
    index = -1;
    while (++index < start) {
      otherArgs[index] = args[index];
    }
    otherArgs[start] = array;
    return apply(func, this, otherArgs);
  };
}
```
- example usage
```shell
...
* @since 4.0.0
* @category Function
* @param {Function} func The function to apply a rest parameter to.
* @param {number} [start=func.length-1] The start position of the rest parameter.
* @returns {Function} Returns the new function.
* @example
*
* var say = _.rest(function(what, names) {
*   return what + ' ' + _.initial(names).join(', ') +
*     (_.size(names) > 1 ? ', & ' : '') + _.last(names);
* });
*
* say('hello', 'fred', 'barney', 'pebbles');
* // => 'hello fred, barney, & pebbles'
*/
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.stubArray"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>stubArray ()](#apidoc.element.bs-html-injector.lodash_custom.stubArray)
- description and source-code
```javascript
function stubArray() {
  return [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.stubFalse"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>stubFalse ()](#apidoc.element.bs-html-injector.lodash_custom.stubFalse)
- description and source-code
```javascript
function stubFalse() {
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.toFinite"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>toFinite (value)](#apidoc.element.bs-html-injector.lodash_custom.toFinite)
- description and source-code
```javascript
function toFinite(value) {
  if (!value) {
    return value === 0 ? value : 0;
  }
  value = toNumber(value);
  if (value === INFINITY || value === -INFINITY) {
    var sign = (value < 0 ? -1 : 1);
    return sign * MAX_INTEGER;
  }
  return value === value ? value : 0;
}
```
- example usage
```shell
...
* @memberOf _
* @since 4.12.0
* @category Lang
* @param {*} value The value to convert.
* @returns {number} Returns the converted number.
* @example
*
* _.toFinite(3.2);
* // => 3.2
*
* _.toFinite(Number.MIN_VALUE);
* // => 5e-324
*
* _.toFinite(Infinity);
* // => 1.7976931348623157e+308
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.toInteger"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>toInteger (value)](#apidoc.element.bs-html-injector.lodash_custom.toInteger)
- description and source-code
```javascript
function toInteger(value) {
  var result = toFinite(value),
      remainder = result % 1;

  return result === result ? (remainder ? result - remainder : result) : 0;
}
```
- example usage
```shell
...
* @memberOf _
* @since 4.0.0
* @category Lang
* @param {*} value The value to convert.
* @returns {number} Returns the converted integer.
* @example
*
* _.toInteger(3.2);
* // => 3
*
* _.toInteger(Number.MIN_VALUE);
* // => 0
*
* _.toInteger(Infinity);
* // => 1.7976931348623157e+308
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.toNumber"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>toNumber (value)](#apidoc.element.bs-html-injector.lodash_custom.toNumber)
- description and source-code
```javascript
function toNumber(value) {
  if (typeof value == 'number') {
    return value;
  }
  if (isSymbol(value)) {
    return NAN;
  }
  if (isObject(value)) {
    var other = isFunction(value.valueOf) ? value.valueOf() : value;
    value = isObject(other) ? (other + '') : other;
  }
  if (typeof value != 'string') {
    return value === 0 ? value : +value;
  }
  value = value.replace(reTrim, '');
  var isBinary = reIsBinary.test(value);
  return (isBinary || reIsOctal.test(value))
    ? freeParseInt(value.slice(2), isBinary ? 2 : 8)
    : (reIsBadHex.test(value) ? NAN : +value);
}
```
- example usage
```shell
...
* @memberOf _
* @since 4.0.0
* @category Lang
* @param {*} value The value to process.
* @returns {number} Returns the number.
* @example
*
* _.toNumber(3.2);
* // => 3.2
*
* _.toNumber(Number.MIN_VALUE);
* // => 5e-324
*
* _.toNumber(Infinity);
* // => Infinity
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.toString"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>toString (value)](#apidoc.element.bs-html-injector.lodash_custom.toString)
- description and source-code
```javascript
function toString(value) {
  return value == null ? '' : baseToString(value);
}
```
- example usage
```shell
...
* @memberOf _
* @since 4.0.0
* @category Lang
* @param {*} value The value to process.
* @returns {string} Returns the string.
* @example
*
* _.toString(null);
* // => ''
*
* _.toString(-0);
* // => '-0'
*
* _.toString([1, 2, 3]);
* // => '1,2,3'
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.uniq"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>uniq (array)](#apidoc.element.bs-html-injector.lodash_custom.uniq)
- description and source-code
```javascript
function uniq(array) {
  return (array && array.length)
    ? baseUniq(array)
    : [];
}
```
- example usage
```shell
...
     */
    function addUiEvents () {

var ui = bs.io.of(bs.ui.config.getIn(["socket", "namespace"]));

bs.ui.listen(config.PLUGIN_NAME, {
    "restriction:add": function (data) {
        opts.restrictions = _.uniq(opts.restrictions.concat([data]));
        updateOptions(opts);
    },
    "restriction:remove": function (data) {
        opts.restrictions = _.without(opts.restrictions, data);
        updateOptions(opts);
    }
});
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.uniqBy"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>uniqBy (array, iteratee)](#apidoc.element.bs-html-injector.lodash_custom.uniqBy)
- description and source-code
```javascript
function uniqBy(array, iteratee) {
  return (array && array.length)
    ? baseUniq(array, getIteratee(iteratee))
    : [];
}
```
- example usage
```shell
...

module.exports = {
/**
 * @param {Array} differences
 * @returns {Array}
 */
removeDupes: function(differences) {
    return _.uniqBy(differences, "node");
},

/**
 * @param diffs
 * @param excludeList
 * @returns {*}
 */
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.values"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>values (object)](#apidoc.element.bs-html-injector.lodash_custom.values)
- description and source-code
```javascript
function values(object) {
  return object ? baseValues(object, keys(object)) : [];
}
```
- example usage
```shell
...
 * function Foo() {
 *   this.a = 1;
 *   this.b = 2;
 * }
 *
 * Foo.prototype.c = 3;
 *
 * _.values(new Foo);
 * // => [1, 2] (iteration order is not guaranteed)
 *
 * _.values('hi');
 * // => ['h', 'i']
 */
function values(object) {
  return object ? baseValues(object, keys(object)) : [];
...
```

#### <a name="apidoc.element.bs-html-injector.lodash_custom.without"></a>[function <span class="apidocSignatureSpan">bs-html-injector.lodash_custom.</span>without ()](#apidoc.element.bs-html-injector.lodash_custom.without)
- description and source-code
```javascript
without = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      array = Array(length);

  while (++index < length) {
    array[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, array);
    case 1: return func.call(this, args[0], array);
    case 2: return func.call(this, args[0], args[1], array);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = array;
  return apply(func, this, otherArgs);
}
```
- example usage
```shell
...

bs.ui.listen(config.PLUGIN_NAME, {
    "restriction:add": function (data) {
        opts.restrictions = _.uniq(opts.restrictions.concat([data]));
        updateOptions(opts);
    },
    "restriction:remove": function (data) {
        opts.restrictions = _.without(opts.restrictions, data);
        updateOptions(opts);
    }
});

function updateOptions (opts) {
    bs.events.emit("plugins:opts", {
        name: config.PLUGIN_NAME,
...
```



# <a name="apidoc.module.bs-html-injector.utils"></a>[module bs-html-injector.utils](#apidoc.module.bs-html-injector.utils)

#### <a name="apidoc.element.bs-html-injector.utils.removeDupes"></a>[function <span class="apidocSignatureSpan">bs-html-injector.utils.</span>removeDupes (differences)](#apidoc.element.bs-html-injector.utils.removeDupes)
- description and source-code
```javascript
removeDupes = function (differences) {
    return _.uniqBy(differences, "node");
}
```
- example usage
```shell
...
    }

    var newDom  = createDom(item1);
    var results = compareDoms(item2, newDom, opts);

    if (results.length) {
        results = results.map(function (result) {
            result.diffs = utils.removeDupes(result.diffs);
            result.diffs = utils.removeExcluded(result.diffs, opts.excludedTags);
            return result;
        });
    }

    return results;
};
...
```

#### <a name="apidoc.element.bs-html-injector.utils.removeExcluded"></a>[function <span class="apidocSignatureSpan">bs-html-injector.utils.</span>removeExcluded (diffs, excludeList)](#apidoc.element.bs-html-injector.utils.removeExcluded)
- description and source-code
```javascript
removeExcluded = function (diffs, excludeList) {
    return _.filter(diffs, function (item) {
        return !_.includes(excludeList, item.tagName);
    });
}
```
- example usage
```shell
...

    var newDom  = createDom(item1);
    var results = compareDoms(item2, newDom, opts);

    if (results.length) {
        results = results.map(function (result) {
            result.diffs = utils.removeDupes(result.diffs);
            result.diffs = utils.removeExcluded(result.diffs, opts.excludedTags);
            return result;
        });
    }

    return results;
};
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
