Insights Graph
==============

A customized force layout written with d3.js. Demo [here](http://ignacioola.github.com/insights-graph/demo/)

## Downloads:
* Version packaged with dependencies: [insights.packaged.js](https://raw.github.com/ignacioola/insights-graph/master/dist/insights.packaged.js)
* Version without dependencies: [insights.js](https://raw.github.com/ignacioola/insights-graph/master/dist/insights.js)

## Stylesheet
* A default optional stylesheet is available: [insights-default.css](https://raw.github.com/ignacioola/insights-graph/master/dist/insights-default.css)

## Dependencies:
* [d3.js](https://github.com/mbostock/d3) (tested with version 2.10.3)
* [underscore.js](https://github.com/documentcloud/underscore/) (tested with version 1.4.3)
* [Mustache.js](https://github.com/janl/mustache.js) (tested with version 0.7.1)

## Minimal input example

```javascript
var nodes = [
    {
        id: 1,
        text: "apple",
        size: 9,
        cluster: 5,
        count: 1034
    },
    {
        id: 2,
        text: "google",
        size: 7,
        cluster: 2,
        count: 534
    },
    {
        id: 3,
        text: "microsoft",
        size: 5,
        cluster: 1,
        count: 432
    }
];

var links = [
    [ 1, 2 ], // [ source.id, target.id ]
    [ 2, 3 ],
    [ 1, 3 ]
];
```

## How to use it ?

```javascript
var el = document.getElementById("container");
new InsightsGraph(el, nodes, links)
```

## Adding an onRendered callback

```javascript
new InsightsGraph(el, nodes, links, {
    onRendered: function() {
        // hide loader
    }
});
```
