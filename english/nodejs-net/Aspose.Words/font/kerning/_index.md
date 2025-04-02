---
title: Font.kerning property
linktitle: kerning property
articleTitle: kerning property
second_title: Aspose.Words for NodeJs
description: "Font.kerning property. Gets or sets the font size at which kerning starts."
type: docs
weight: 180
url: /nodejs-net/Aspose.Words/font/kerning/
---

## Font.kerning property

Gets or sets the font size at which kerning starts.


```js
get kerning(): number
```

### Examples

Shows how to specify the font size at which kerning begins to take effect.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.font.name = "Arial Black";

// Set the builder's font size, and minimum size at which kerning will take effect.
// The font size falls below the kerning threshold, so the run bellow will not have kerning.
builder.font.size = 18;
builder.font.kerning = 24;

builder.writeln("TALLY. (Kerning not applied)");

// Set the kerning threshold so that the builder's current font size is above it.
// Any text we add from this point will have kerning applied. The spaces between characters
// will be adjusted, normally resulting in a slightly more aesthetically pleasing text run.
builder.font.kerning = 12;

builder.writeln("TALLY. (Kerning applied)");

doc.save(base.artifactsDir + "Font.kerning.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

