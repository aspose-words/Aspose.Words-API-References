---
title: ParagraphFormat.baselineAlignment property
linktitle: baselineAlignment property
articleTitle: baselineAlignment property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.baselineAlignment property. Gets or sets fonts vertical position on a line."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/paragraphformat/baselineAlignment/
---

## ParagraphFormat.baselineAlignment property

Gets or sets fonts vertical position on a line.


```js
get baselineAlignment(): Aspose.Words.BaselineAlignment
```

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

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

