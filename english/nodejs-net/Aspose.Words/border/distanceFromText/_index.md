---
title: Border.distanceFromText property
linktitle: distanceFromText property
articleTitle: distanceFromText property
second_title: Aspose.Words for Node.js
description: "Border.distanceFromText property. Gets or sets distance of the border from text or from the page edge in points."
type: docs
weight: 20
url: /nodejs-net/aspose.words/border/distanceFromText/
---

## Border.distanceFromText property

Gets or sets distance of the border from text or from the page edge in points.


```js
get distanceFromText(): number
```

### Remarks

Has no effect and will be automatically reset to zero for borders of table cells.




### Examples

Shows how to create a wide blue band border at the top of the first page.

```js
let doc = new aw.Document();

let pageSetup = doc.sections.at(0).pageSetup;
pageSetup.borderAlwaysInFront = false;
pageSetup.borderDistanceFrom = aw.PageBorderDistanceFrom.PageEdge;
pageSetup.borderAppliesTo = aw.PageBorderAppliesTo.FirstPage;

let border = pageSetup.borders.at(aw.BorderType.Top);
border.lineStyle = aw.LineStyle.Single;
border.lineWidth = 30;
border.color = "#0000FF";
border.distanceFromText = 0;

doc.save(base.artifactsDir + "PageSetup.PageBorderProperties.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Border](../)
* property [PageSetup.borderDistanceFrom](../../pagesetup/borderDistanceFrom/)

