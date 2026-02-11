---
title: TextEffect enumeration
linktitle: TextEffect enumeration
articleTitle: TextEffect enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.TextEffect enumeration. Animation effect for text runs."
type: docs
weight: 1420
url: /nodejs-net/aspose.words/texteffect/
---

## TextEffect enumeration

Animation effect for text runs.


### Members

| Name | Description |
| --- | --- |
| None |  |
| LasVegasLights |  |
| BlinkingBackground |  |
| SparkleText |  |
| MarchingBlackAnts |  |
| MarchingRedAnts |  |
| Shimmer |  |

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

* module [Aspose.Words](../)

