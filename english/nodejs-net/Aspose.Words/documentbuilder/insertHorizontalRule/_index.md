---
title: DocumentBuilder.insertHorizontalRule method
linktitle: insertHorizontalRule method
articleTitle: insertHorizontalRule method
second_title: Aspose.Words for Node.js
description: "DocumentBuilder.insertHorizontalRule method. Inserts a horizontal rule shape into the document."
type: docs
weight: 370
url: /nodejs-net/aspose.words/documentbuilder/insertHorizontalRule/
---

## insertHorizontalRule() {#default}

Inserts a horizontal rule shape into the document.


```js
insertHorizontalRule()
```

### Returns

The shape that is a horizontal rule.


### Examples

Shows how to insert a horizontal rule shape, and customize its formatting.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
let shape = builder.insertHorizontalRule();

let horizontalRuleFormat = shape.horizontalRuleFormat;
horizontalRuleFormat.alignment = aw.Drawing.HorizontalRuleAlignment.Center;
horizontalRuleFormat.widthPercent = 70;
horizontalRuleFormat.height = 3;
horizontalRuleFormat.color = "#0000FF";
horizontalRuleFormat.noShade = true;

expect(shape.isHorizontalRule).toEqual(true);
expect(shape.horizontalRuleFormat.noShade).toEqual(true);
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

