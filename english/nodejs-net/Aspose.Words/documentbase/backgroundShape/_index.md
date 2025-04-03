---
title: DocumentBase.backgroundShape property
linktitle: backgroundShape property
articleTitle: backgroundShape property
second_title: Aspose.Words for NodeJs
description: "DocumentBase.backgroundShape property. Gets or sets the background shape of the document"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words/documentbase/backgroundShape/
---

## DocumentBase.backgroundShape property

Gets or sets the background shape of the document. Can be ``None``.



```js
get backgroundShape(): Aspose.Words.Drawing.Shape
```

### Remarks

Microsoft Word allows only a shape that has its [ShapeBase.shapeType](../../../aspose.words.drawing/shapebase/shapeType/) property equal
to [ShapeType.Rectangle](../../../aspose.words.drawing/shapetype/#Rectangle) to be used as a background shape for a document.

Microsoft Word supports only the fill properties of a background shape. All other properties
are ignored.

Setting this property to a non-null value will also set the [ViewOptions.displayBackgroundShape](../../../aspose.words.settings/viewoptions/displayBackgroundShape/) to ``True``.




### Examples

Shows how to set a background shape for every page of a document.

```js
let doc = new aw.Document();

expect(doc.backgroundShape).toBe(null);

// The only shape type that we can use as a background is a rectangle.
let shapeRectangle = new aw.Drawing.Shape(doc, aw.Drawing.ShapeType.Rectangle);

// There are two ways of using this shape as a page background.
// 1 -  A flat color:
shapeRectangle.fillColor = "#ADD8E6";
doc.backgroundShape = shapeRectangle;

doc.save(base.artifactsDir + "DocumentBase.backgroundShape.FlatColor.docx");

// 2 -  An image:
shapeRectangle = new aw.Drawing.Shape(doc, aw.Drawing.ShapeType.Rectangle);
shapeRectangle.imageData.setImage(base.imageDir + "Transparent background logo.png");

// Adjust the image's appearance to make it more suitable as a watermark.
shapeRectangle.imageData.contrast = 0.2;
shapeRectangle.imageData.brightness = 0.7;

doc.backgroundShape = shapeRectangle;

expect(doc.backgroundShape.hasImage).toEqual(true);

let saveOptions = new aw.Saving.PdfSaveOptions();
saveOptions.CacheBackgroundGraphics = false;

// Microsoft Word does not support shapes with images as backgrounds,
// but we can still see these backgrounds in other save formats such as .pdf.
doc.save(base.artifactsDir + "DocumentBase.backgroundShape.image.pdf", saveOptions);
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBase](../)
* property [ViewOptions.displayBackgroundShape](../../../aspose.words.settings/viewoptions/displayBackgroundShape/)
* property [DocumentBase.pageColor](../pageColor/)

