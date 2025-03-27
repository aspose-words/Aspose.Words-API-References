---
title: Fill.foreTintAndShade property
linktitle: foreTintAndShade property
articleTitle: foreTintAndShade property
second_title: Aspose.Words for NodeJs
description: "Fill.foreTintAndShade property. Gets or sets a double value that lightens or darkens the foreground color."
type: docs
weight: 90
url: /nodejs-net/Aspose.Words.Drawing/fill/foreTintAndShade/
---

## Fill.foreTintAndShade property

Gets or sets a double value that lightens or darkens the foreground color.


```js
get foreTintAndShade(): number
```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throw if set this property to a value less than -1 or more than 1. |

### Remarks

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property.

Zero (0) is neutral.




### Examples

Shows how to manage lightening and darkening foreground font color.

```js
let doc = new aw.Document(base.myDir + "Big document.docx");

let textFill = doc.firstSection.body.firstParagraph.runs.at(0).font.fill;
textFill.foreThemeColor = aw.Themes.ThemeColor.Accent1;
if (textFill.foreTintAndShade == 0)
  textFill.foreTintAndShade = 0.5;

doc.save(base.artifactsDir + "Shape.FillTintAndShade.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [Fill](../)

