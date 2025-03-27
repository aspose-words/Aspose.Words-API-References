---
title: Font.complexScript property
linktitle: complexScript property
articleTitle: complexScript property
second_title: Aspose.Words for NodeJs
description: "Font.complexScript property. Specifies whether the contents of this run shall be treated as complex script text regardless of their Unicode character values when determining the formatting for this run."
type: docs
weight: 80
url: /nodejs-net/Aspose.Words/font/complexScript/
---

## Font.complexScript property

Specifies whether the contents of this run shall be treated as complex script text regardless
of their Unicode character values when determining the formatting for this run.


```js
get complexScript(): boolean
```

### Examples

Shows how to add text that is always treated as complex script.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.complexScript = true;

builder.writeln("Text treated as complex script.");

doc.save(base.artifactsDir + "Font.complexScript.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

