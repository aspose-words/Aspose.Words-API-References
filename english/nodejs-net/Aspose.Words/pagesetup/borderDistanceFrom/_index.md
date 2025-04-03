---
title: PageSetup.borderDistanceFrom property
linktitle: borderDistanceFrom property
articleTitle: borderDistanceFrom property
second_title: Aspose.Words for NodeJs
description: "PageSetup.borderDistanceFrom property. Gets or sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds."
type: docs
weight: 40
url: /nodejs-net/aspose.words/pagesetup/borderDistanceFrom/
---

## PageSetup.borderDistanceFrom property

Gets or sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds.


```js
get borderDistanceFrom(): Aspose.Words.PageBorderDistanceFrom
```

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
* class [PageSetup](../)

