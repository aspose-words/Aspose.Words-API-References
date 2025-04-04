---
title: ShapeBase.isTopLevel property
linktitle: isTopLevel property
articleTitle: isTopLevel property
second_title: Aspose.Words for Node.js
description: "ShapeBase.isTopLevel property. Returns ``true`` if this shape is not a child of a group shape."
type: docs
weight: 320
url: /nodejs-net/aspose.words.drawing/shapebase/isTopLevel/
---

## ShapeBase.isTopLevel property

Returns ``true`` if this shape is not a child of a group shape.



```js
get isTopLevel(): boolean
```

### Examples

Shows how to tell whether a shape is a part of a group shape.

```js
let doc = new aw.Document();

let shape = new aw.Drawing.Shape(doc, aw.Drawing.ShapeType.Rectangle);
shape.width = 200;
shape.height = 200;
shape.wrapType = aw.Drawing.WrapType.None;

// A shape by default is not part of any group shape, and therefore has the "IsTopLevel" property set to "true".
expect(shape.isTopLevel).toEqual(true);

let group = new aw.Drawing.GroupShape(doc);
group.appendChild(shape);

// Once we assimilate a shape into a group shape, the "IsTopLevel" property changes to "false".
expect(shape.isTopLevel).toEqual(false);
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

