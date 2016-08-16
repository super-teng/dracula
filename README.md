# Graph Dracula - a JavaScript Graph Library

Graph Dracula is a set of tools to display and layout interactive graphs,
along with various related algorithms.

No Flash, no Java, no plug-ins. Just plain JavaScript and SVG.

The code is released under the MIT license, so commercial use is not a problem.

Creating a graph is simple! You can also customise anything easily.

The code looks like this:

    var g = new Graph();

    g.addEdge('strawberry', 'cherry');

    var layouter = new Graph.Layout.Spring(g);
    layouter.layout();

    var renderer = new Graph.Renderer.Raphael('canvas', g, 400, 300);
    renderer.draw();

## Installation

First, install the dependencies:

    npm install --save graphdracula raphael

Second, create an html file with a tag having the ID `paper`.

Third, require graphdracula (via browserify or webpack):

    var Dracula = require('graphdracula');

    var Graph = Dracula.Graph;
    var Renderer = Dracula.Renderer.Raphael;
    var Layout = Dracula.Layout.Spring;

    var graph = new Graph();

    graph.addEdge('Banana', 'Apple');
    graph.addEdge('Apple', 'Kiwi');
    graph.addEdge('Apple', 'Dragonfruit');
    graph.addEdge('Dragonfruit', 'Banana');
    graph.addEdge('Kiwi', 'Banana');

    var layout = new Layout(graph)
    var renderer = new Renderer('#paper', graph, 400, 300);
    renderer.draw()


## How To Develop

```
npm i
npm start
```
