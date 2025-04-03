---
title: PdfSaveOptions.clone method
linktitle: clone method
articleTitle: clone method
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.clone method. Creates a deep clone of this object."
type: docs
weight: 370
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/clone/
---

## clone() {#default}

Creates a deep clone of this object.


```js
clone()
```

### Examples

Shows how to update all the fields in a document immediately before saving it to PDF.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert text with PAGE and NUMPAGES fields. These fields do not display the correct value in real time.
// We will need to manually update them using updating methods such as "Field.update()", and "Document.updateFields()"
// each time we need them to display accurate values.
builder.write("Page ");
builder.insertField("PAGE", "");
builder.write(" of ");
builder.insertField("NUMPAGES", "");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Hello World!");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Set the "UpdateFields" property to "false" to not update all the fields in a document right before a save operation.
// This is the preferable option if we know that all our fields will be up to date before saving.
// Set the "UpdateFields" property to "true" to iterate through all the document
// fields and update them before we save it as a PDF. This will make sure that all the fields will display
// the most accurate values in the PDF.
options.updateFields = updateFields;

// We can clone PdfSaveOptions objects.
expect(options).not.toBe(options.clone());

doc.save(base.artifactsDir + "PdfSaveOptions.updateFields.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

