---
title: Chart.sourceFullName property
linktitle: sourceFullName property
articleTitle: sourceFullName property
second_title: Aspose.Words for NodeJs
description: "Chart.sourceFullName property. Gets the path and name of an xls/xlsx file this chart is linked to."
type: docs
weight: 100
url: /nodejs-net/Aspose.Words.Drawing/chart/sourceFullName/
---

## Chart.sourceFullName property

Gets the path and name of an xls/xlsx file this chart is linked to.


```js
get sourceFullName(): string
```

### Examples

Shows how to get/set the full name of the external xls/xlsx document if the chart is linked.

```js
let doc = new aw.Document(base.myDir + "Shape with linked chart.docx");

let shape = doc.getShape(0, true);

let sourceFullName = shape.chart.sourceFullName;
expect(sourceFullName.includes("Examples\\Data\\Spreadsheet.xlsx")).toEqual(true);
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [Chart](../)

