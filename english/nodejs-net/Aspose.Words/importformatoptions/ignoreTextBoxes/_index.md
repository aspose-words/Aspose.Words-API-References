---
title: ImportFormatOptions.ignoreTextBoxes property
linktitle: ignoreTextBoxes property
articleTitle: ignoreTextBoxes property
second_title: Aspose.Words for NodeJs
description: "ImportFormatOptions.ignoreTextBoxes property. Gets or sets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KeepSourceFormatting](../../importformatmode/#KeepSourceFormatting) mode is used"
type: docs
weight: 50
url: /nodejs-net/Aspose.Words/importformatoptions/ignoreTextBoxes/
---

## ImportFormatOptions.ignoreTextBoxes property

Gets or sets a boolean value that specifies that source formatting of textboxes content ignored
if [ImportFormatMode.KeepSourceFormatting](../../importformatmode/#KeepSourceFormatting) mode is used.
The default value is ``true``.



```js
get ignoreTextBoxes(): boolean
```

### Examples

Shows how to manage text box formatting while appending a document.

```js
// Create a document that will have nodes from another document inserted into it.
let dstDoc = new aw.Document();
let builder = new aw.DocumentBuilder(dstDoc);

builder.writeln("Hello world!");

// Create another document with a text box, which we will import into the first document.
let srcDoc = new aw.Document();
builder = new aw.DocumentBuilder(srcDoc);

let textBox = builder.insertShape(aw.Drawing.ShapeType.TextBox, 300, 100);
builder.moveTo(textBox.firstParagraph);
builder.paragraphFormat.style.font.name = "Courier New";
builder.paragraphFormat.style.font.size = 24;
builder.write("Textbox contents");

// Set a flag to specify whether to clear or preserve text box formatting
// while importing them to other documents.
let importFormatOptions = new aw.ImportFormatOptions();
importFormatOptions.ignoreTextBoxes = ignoreTextBoxes;

// Import the text box from the source document into the destination document,
// and then verify whether we have preserved the styling of its text contents.
let importer = new aw.NodeImporter(srcDoc, dstDoc, aw.ImportFormatMode.KeepSourceFormatting, importFormatOptions);
let importedTextBox = importer.importNode(textBox, true).asShape();
dstDoc.firstSection.body.paragraphs.at(1).appendChild(importedTextBox);

if (ignoreTextBoxes)
{
  expect(importedTextBox.firstParagraph.runs.at(0).font.size).toEqual(12.0);
  expect(importedTextBox.firstParagraph.runs.at(0).font.name).toEqual("Times New Roman");
}
else
{
  expect(importedTextBox.firstParagraph.runs.at(0).font.size).toEqual(24.0);
  expect(importedTextBox.firstParagraph.runs.at(0).font.name).toEqual("Courier New");
}

dstDoc.save(base.artifactsDir + "DocumentBuilder.ignoreTextBoxes.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ImportFormatOptions](../)

