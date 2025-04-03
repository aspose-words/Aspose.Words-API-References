---
title: OoxmlCompliance enumeration
linktitle: OoxmlCompliance enumeration
articleTitle: OoxmlCompliance enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.OoxmlCompliance enumeration. Allows to specify which OOXML specification will be used when saving in the DOCX format."
type: docs
weight: 520
url: /nodejs-net/aspose.words.saving/ooxmlcompliance/
---

## OoxmlCompliance enumeration

Allows to specify which OOXML specification will be used when saving in the DOCX format.


### Members

| Name | Description |
| --- | --- |
| Ecma376_2006 | ECMA-376 1st Edition, 2006. |
| Iso29500_2008_Transitional | ISO/IEC 29500:2008 Transitional compliance level. |
| Iso29500_2008_Strict | ISO/IEC 29500:2008 Strict compliance level. |

### Examples

Shows how to insert DML shapes into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Below are two wrapping types that shapes may have.
// 1 -  Floating:
builder.insertShape(aw.Drawing.ShapeType.TopCornersRounded, aw.Drawing.RelativeHorizontalPosition.Page, 100,
    aw.Drawing.RelativeVerticalPosition.Page, 100, 50, 50, aw.Drawing.WrapType.None);

// 2 -  Inline:
builder.insertShape(aw.Drawing.ShapeType.DiagonalCornersRounded, 50, 50);

// If you need to create "non-primitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
// then save the document with "Strict" or "Transitional" compliance, which allows saving shape as DML.
let saveOptions = new aw.Saving.OoxmlSaveOptions(aw.SaveFormat.Docx);
saveOptions.compliance = aw.Saving.OoxmlCompliance.Iso29500_2008_Transitional;

doc.save(base.artifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

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

Shows how to configure a list to restart numbering at each section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

doc.lists.add(aw.Lists.ListTemplate.NumberDefault);

let list = doc.lists.at(0);
list.isRestartAtEachSection = restartListAtEachSection;

// The "IsRestartAtEachSection" property will only be applicable when
// the document's OOXML compliance level is to a standard that is newer than "OoxmlComplianceCore.Ecma376".
let options = new aw.Saving.OoxmlSaveOptions();
options.compliance = aw.Saving.OoxmlCompliance.Iso29500_2008_Transitional;

builder.listFormat.list = list;

builder.writeln("List item 1");
builder.writeln("List item 2");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.writeln("List item 3");
builder.writeln("List item 4");

doc.save(base.artifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new aw.Document(base.artifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

expect(doc.lists.at(0).isRestartAtEachSection).toEqual(restartListAtEachSection);
```

### See Also

* module [Aspose.Words.Saving](../)

