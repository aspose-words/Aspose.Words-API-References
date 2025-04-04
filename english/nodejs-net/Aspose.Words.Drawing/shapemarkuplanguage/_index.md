---
title: ShapeMarkupLanguage enumeration
linktitle: ShapeMarkupLanguage enumeration
articleTitle: ShapeMarkupLanguage enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.ShapeMarkupLanguage enumeration. Specifies Markup language used for the shape."
type: docs
weight: 400
url: /nodejs-net/aspose.words.drawing/shapemarkuplanguage/
---

## ShapeMarkupLanguage enumeration

Specifies Markup language used for the shape.


### Members

| Name | Description |
| --- | --- |
| Dml | Drawing Markup Language is used to define the shape. |
| Vml | Vector Markup Language is used to define the shape. |

### Examples

Shows how to set an OOXML compliance specification for a saved document to adhere to.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// If we configure compatibility options to comply with Microsoft Word 2003,
// inserting an image will define its shape using VML.
doc.compatibilityOptions.optimizeFor(aw.Settings.MsWordVersion.Word2003);
builder.insertImage(base.imageDir + "Transparent background logo.png");

expect(doc.getShape(0, true).markupLanguage).toEqual(aw.Drawing.ShapeMarkupLanguage.Vml);

// The "ISO/IEC 29500:2008" OOXML standard does not support VML shapes.
// If we set the "Compliance" property of the SaveOptions object to "OoxmlCompliance.Iso29500_2008_Strict",
// any document we save while passing this object will have to follow that standard. 
let saveOptions = new aw.Saving.OoxmlSaveOptions();
saveOptions.compliance = aw.Saving.OoxmlCompliance.Iso29500_2008_Strict;
saveOptions.saveFormat = aw.SaveFormat.Docx;

doc.save(base.artifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Our saved document defines the shape using DML to adhere to the "ISO/IEC 29500:2008" OOXML standard.
doc = new aw.Document(base.artifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

expect(doc.getShape(0, true).markupLanguage).toEqual(aw.Drawing.ShapeMarkupLanguage.Dml);
```

### See Also

* module [Aspose.Words.Drawing](../)

