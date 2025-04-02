---
title: Font.spacing property
linktitle: spacing property
articleTitle: spacing property
second_title: Aspose.Words for NodeJs
description: "Font.spacing property. Returns or sets the spacing (in points) between characters ."
type: docs
weight: 390
url: /nodejs-net/Aspose.Words/font/spacing/
---

## Font.spacing property

Returns or sets the spacing (in points) between characters .


```js
get spacing(): number
```

### Examples

Shows how to set horizontal scaling and spacing for characters.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Add run of text and increase character width to 150%.
builder.font.scaling = 150;
builder.writeln("Wide characters");

// Add run of text and add 1pt of extra horizontal spacing between each character.
builder.font.spacing = 1;
builder.writeln("Expanded by 1pt");

// Add run of text and bring characters closer together by 1pt.
builder.font.spacing = -1;
builder.writeln("Condensed by 1pt");

doc.save(base.artifactsDir + "Font.ScalingSpacing.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

