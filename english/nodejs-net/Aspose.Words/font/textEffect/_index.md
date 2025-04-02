---
title: Font.textEffect property
linktitle: textEffect property
articleTitle: textEffect property
second_title: Aspose.Words for NodeJs
description: "Font.textEffect property. Gets or sets the font animation effect."
type: docs
weight: 460
url: /nodejs-net/Aspose.Words/font/textEffect/
---

## Font.textEffect property

Gets or sets the font animation effect.


```js
get textEffect(): Aspose.Words.TextEffect
```

### Examples

Shows how to apply a visual effect to a run.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.size = 36;
builder.font.textEffect = aw.TextEffect.SparkleText;

builder.writeln("Text with a sparkle effect.");

// Older versions of Microsoft Word only support font animation effects.
doc.save(base.artifactsDir + "Font.SparklingText.doc");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

