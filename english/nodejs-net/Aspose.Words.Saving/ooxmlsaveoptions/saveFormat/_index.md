---
title: OoxmlSaveOptions.saveFormat property
linktitle: saveFormat property
articleTitle: saveFormat property
second_title: Aspose.Words for Node.js
description: "OoxmlSaveOptions.saveFormat property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 70
url: /nodejs-net/aspose.words.saving/ooxmlsaveoptions/saveFormat/
---

## OoxmlSaveOptions.saveFormat property

Specifies the format in which the document will be saved if this save options object is used.
Can be [SaveFormat.Docx](../../../aspose.words/saveformat/#Docx), [SaveFormat.Docm](../../../aspose.words/saveformat/#Docm),
[SaveFormat.Dotx](../../../aspose.words/saveformat/#Dotx), [SaveFormat.Dotm](../../../aspose.words/saveformat/#Dotm) or [SaveFormat.FlatOpc](../../../aspose.words/saveformat/#FlatOpc).



```js
get saveFormat(): Aspose.Words.SaveFormat
```

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

* module [Aspose.Words.Saving](../../)
* class [OoxmlSaveOptions](../)

