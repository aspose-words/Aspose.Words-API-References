---
title: PageSetup.borders property
linktitle: borders property
articleTitle: borders property
second_title: Aspose.Words for NodeJs
description: "PageSetup.borders property. Gets a collection of the page borders."
type: docs
weight: 70
url: /nodejs-net/aspose.words/pagesetup/borders/
---

## PageSetup.borders property

Gets a collection of the page borders.


```js
get borders(): Aspose.Words.BorderCollection
```

### Examples

Shows how to create green wavy page border with a shadow.

```js
let doc = new aw.Document();
let pageSetup = doc.sections.at(0).pageSetup;

pageSetup.borders.lineStyle = aw.LineStyle.DoubleWave;
pageSetup.borders.lineWidth = 2;
pageSetup.borders.color = "#008000";
pageSetup.borders.distanceFromText = 24;
pageSetup.borders.shadow = true;

doc.save(base.artifactsDir + "PageSetup.PageBorders.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

