---
title: Border.shadow property
linktitle: shadow property
articleTitle: shadow property
second_title: Aspose.Words for NodeJs
description: "Border.shadow property. Gets or sets a value indicating whether the border has a shadow."
type: docs
weight: 60
url: /nodejs-net/aspose.words/border/shadow/
---

## Border.shadow property

Gets or sets a value indicating whether the border has a shadow.


```js
get shadow(): boolean
```

### Remarks

In Microsoft Word, for a border to have a shadow, the borders on all four sides
(left, top, right and bottom) should be of the same type, width, color and all should have
the Shadow property set to ``true``.




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
* class [Border](../)

