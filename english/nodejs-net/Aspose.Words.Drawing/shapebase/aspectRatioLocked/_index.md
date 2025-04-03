---
title: ShapeBase.aspectRatioLocked property
linktitle: aspectRatioLocked property
articleTitle: aspectRatioLocked property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.aspectRatioLocked property. Specifies whether the shape's aspect ratio is locked."
type: docs
weight: 40
url: /nodejs-net/aspose.words.drawing/shapebase/aspectRatioLocked/
---

## ShapeBase.aspectRatioLocked property

Specifies whether the shape's aspect ratio is locked.


```js
get aspectRatioLocked(): boolean
```

### Remarks

The default value depends on the [ShapeType](../../shapetype/), for the [ShapeType.Image](../../shapetype/#Image) it is ``true``
but for the other shape types it is ``false``.

Has effect for top level shapes only.




### Examples

Shows how to lock/unlock a shape's aspect ratio.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a shape. If we open this document in Microsoft Word, we can left click the shape to reveal
// eight sizing handles around its perimeter, which we can click and drag to change its size.
let shape = builder.insertImage(base.imageDir + "Logo.jpg");

// Set the "AspectRatioLocked" property to "true" to preserve the shape's aspect ratio
// when using any of the four diagonal sizing handles, which change both the image's height and width.
// Using any orthogonal sizing handles that either change the height or width will still change the aspect ratio.
// Set the "AspectRatioLocked" property to "false" to allow us to
// freely change the image's aspect ratio with all sizing handles.
shape.aspectRatioLocked = lockAspectRatio;

doc.save(base.artifactsDir + "Shape.aspectRatio.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

