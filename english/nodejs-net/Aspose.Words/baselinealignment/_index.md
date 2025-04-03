---
title: BaselineAlignment enumeration
linktitle: BaselineAlignment enumeration
articleTitle: BaselineAlignment enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.BaselineAlignment enumeration. Specifies fonts vertical position on a line."
type: docs
weight: 20
url: /nodejs-net/aspose.words/baselinealignment/
---

## BaselineAlignment enumeration

Specifies fonts vertical position on a line.


### Members

| Name | Description |
| --- | --- |
| Top | Aligns along the top of each font. |
| Center | Aligns the center points of each font. |
| Baseline | Aligns to the baseline of the paragraph. |
| Bottom | Aligns to the bottom of each font. |
| Auto | Baseline is adjusted automatically. |

### Examples

Shows how to set fonts vertical position on a line.

```js
let doc = new aw.Document(base.myDir + "Office math.docx");

let format = doc.firstSection.body.paragraphs.at(0).paragraphFormat;
if (format.baselineAlignment == aw.BaselineAlignment.Auto)
{
  format.baselineAlignment = aw.BaselineAlignment.Top;
}

doc.save(base.artifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### See Also

* module [Aspose.Words](../)

