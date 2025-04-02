---
title: PageSetup.borderAlwaysInFront property
linktitle: borderAlwaysInFront property
articleTitle: borderAlwaysInFront property
second_title: Aspose.Words for NodeJs
description: "PageSetup.borderAlwaysInFront property. Specifies where the page border is positioned relative to intersecting texts and objects."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words/pagesetup/borderAlwaysInFront/
---

## PageSetup.borderAlwaysInFront property

Specifies where the page border is positioned relative to intersecting texts and objects.


```js
get borderAlwaysInFront(): boolean
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

