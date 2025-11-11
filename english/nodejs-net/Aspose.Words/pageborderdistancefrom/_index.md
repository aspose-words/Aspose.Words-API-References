---
title: PageBorderDistanceFrom enumeration
linktitle: PageBorderDistanceFrom enumeration
articleTitle: PageBorderDistanceFrom enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.PageBorderDistanceFrom enumeration. Specifies the positioning of the page border relative to the page margin."
type: docs
weight: 960
url: /nodejs-net/aspose.words/pageborderdistancefrom/
---

## PageBorderDistanceFrom enumeration

Specifies the positioning of the page border relative to the page margin.


### Members

| Name | Description |
| --- | --- |
| Text | Border position is measured from the page margin. |
| PageEdge | Border position is measured from the page edge. |

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

* module [Aspose.Words](../)
* class [PageSetup](../pagesetup/)
* property [PageSetup.borderDistanceFrom](../pagesetup/borderDistanceFrom/)

