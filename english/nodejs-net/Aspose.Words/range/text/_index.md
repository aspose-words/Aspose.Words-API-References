---
title: Range.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for NodeJs
description: "Range.text property. Gets the text of the range."
type: docs
weight: 60
url: /nodejs-net/aspose.words/range/text/
---

## Range.text property

Gets the text of the range.


```js
get text(): string
```

### Remarks

The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).




### Examples

Shows how to get the text contents of all the nodes that a range covers.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Hello world!");

expect(doc.range.text.trim()).toEqual("Hello world!");
```

### See Also

* module [Aspose.Words](../../)
* class [Range](../)

