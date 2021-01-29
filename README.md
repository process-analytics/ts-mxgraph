# A Tiny Typescript Wrapper for mxgraph

**Archived on 2021-01-29**: `ts-mxgraph` was used in [bpmn-visualization](https://github.com/process-analytics/bpmn-visualization-js) until version `0.11.0`,
it has then been replaced by a more standard solution, see [bpmn-visualization Pull Request #1040](https://github.com/process-analytics/bpmn-visualization-js/pull/1040)


## Overview

A tiny wrapper around [mxgraph](https://github.com/jgraph/mxgraph-js) that
provides a configurable TypeScript compatible package.

## Usage
```sh
npm i -D ts-mxgraph
```

```typescript
import { mxgraph, mxgraphFactory } from "ts-mxgraph";

const { mxGraph, mxGraphModel } = mxgraphFactory({
    mxLoadResources: false,
    mxLoadStylesheets: false,
});

const container = document.getElementById("mxgraph-container");
if (container) {
    const model: mxgraph.mxGraphModel = new mxGraphModel();
    const graph: mxgraph.mxGraph = new mxGraph(container, model);
}
```

## License

[Apache 2.0 License](LICENSE)
