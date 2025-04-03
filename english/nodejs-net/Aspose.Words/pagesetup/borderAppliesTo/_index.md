---
title: PageSetup.borderAppliesTo property
linktitle: borderAppliesTo property
articleTitle: borderAppliesTo property
second_title: Aspose.Words for NodeJs
description: "PageSetup.borderAppliesTo property. Specifies which pages the page border is printed on."
type: docs
weight: 30
url: /nodejs-net/aspose.words/pagesetup/borderAppliesTo/
---

## PageSetup.borderAppliesTo property

Specifies which pages the page border is printed on.


```js
get borderAppliesTo(): Aspose.Words.PageBorderAppliesTo
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

