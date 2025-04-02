---
title: Font.highlightColor property
linktitle: highlightColor property
articleTitle: highlightColor property
second_title: Aspose.Words for NodeJs
description: "Font.highlightColor property. Gets or sets the highlight (marker) color."
type: docs
weight: 150
url: /nodejs-net/Aspose.Words/font/highlightColor/
---

## Font.highlightColor property

Gets or sets the highlight (marker) color.


```js
get highlightColor(): string
```

### Examples

Shows how to format a run of text using its font property.

```js
let doc = new aw.Document();
let run = new aw.Run(doc, "Hello world!");

let font = run.font;
font.name = "Courier New";
font.size = 36;
font.highlightColor = "#FFFF00";

doc.firstSection.body.firstParagraph.appendChild(run);
doc.save(base.artifactsDir + "Font.CreateFormattedRun.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

