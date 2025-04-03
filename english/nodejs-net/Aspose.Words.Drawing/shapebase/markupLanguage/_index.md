---
title: ShapeBase.markupLanguage property
linktitle: markupLanguage property
articleTitle: markupLanguage property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.markupLanguage property. Gets MarkupLanguage used for this graphic object."
type: docs
weight: 360
url: /nodejs-net/aspose.words.drawing/shapebase/markupLanguage/
---

## ShapeBase.markupLanguage property

Gets MarkupLanguage used for this graphic object.


```js
get markupLanguage(): Aspose.Words.Drawing.ShapeMarkupLanguage
```

### Examples

Shows how to verify a shape's size and markup language.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertImage(base.imageDir + "Transparent background logo.png");

expect(shape.markupLanguage).toEqual(aw.Drawing.ShapeMarkupLanguage.Dml);
expect(shape.sizeInPoints2).toEqual(new aw.JSSizeF(300, 300));
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

