---
title: PageBorderAppliesTo enumeration
linktitle: PageBorderAppliesTo enumeration
articleTitle: PageBorderAppliesTo enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.PageBorderAppliesTo enumeration. Specifies which pages the page border is printed on."
type: docs
weight: 940
url: /nodejs-net/aspose.words/pageborderappliesto/
---

## PageBorderAppliesTo enumeration

Specifies which pages the page border is printed on.


### Members

| Name | Description |
| --- | --- |
| AllPages | Page border is shown on all pages of the section. |
| FirstPage | Page border is shown on the first page of the section only. |
| OtherPages | Page border is shown on all pages except the first page of the section. |

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
* property [PageSetup.borderAppliesTo](../pagesetup/borderAppliesTo/)

