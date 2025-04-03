---
title: Document.defaultTabStop property
linktitle: defaultTabStop property
articleTitle: defaultTabStop property
second_title: Aspose.Words for NodeJs
description: "Document.defaultTabStop property. Gets or sets the interval (in points) between the default tab stops."
type: docs
weight: 100
url: /nodejs-net/aspose.words/document/defaultTabStop/
---

## Document.defaultTabStop property

Gets or sets the interval (in points) between the default tab stops.


```js
get defaultTabStop(): number
```

### Examples

Shows how to set a custom interval for tab stop positions.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
// Set tab stops to appear every 72 points (1 inch).
builder.document.defaultTabStop = 72;
// Each tab character snaps the text after it to the next closest tab stop position.
builder.writeln("Hello" + aw.ControlChar.tab + "World!");
builder.writeln("Hello" + aw.ControlChar.tabChar + "World!");
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)
* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)

