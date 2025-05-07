---
title: FieldFileName.includeFullPath property
linktitle: includeFullPath property
articleTitle: includeFullPath property
second_title: Aspose.Words for Node.js
description: "FieldFileName.includeFullPath property. Gets or sets whether to include the full file path name."
type: docs
weight: 20
url: /nodejs-net/aspose.words.fields/fieldfilename/includeFullPath/
---

## FieldFileName.includeFullPath property

Gets or sets whether to include the full file path name.


```js
get includeFullPath(): boolean
```

### Examples

Shows how to use FieldOptions to override the default value for the FILENAME field.

```js
let doc = new aw.Document(base.myDir + "Document.docx");
let builder = new aw.DocumentBuilder(doc);

builder.moveToDocumentEnd();
builder.writeln();

// This FILENAME field will display the local system file name of the document we loaded.
let field = builder.insertField(aw.Fields.FieldType.FieldFileName, true).asFieldFileName();
field.update();

expect(field.getFieldCode()).toEqual(" FILENAME ");
expect(field.result).toEqual("Document.docx");

builder.writeln();

// By default, the FILENAME field shows the file's name, but not its full local file system path.
// We can set a flag to make it show the full file path.
field = builder.insertField(aw.Fields.FieldType.FieldFileName, true).asFieldFileName();
field.includeFullPath = true;
field.update();

expect(field.result).toEqual(base.myDir + "Document.docx");

// We can also set a value for this property to
// override the value that the FILENAME field displays.
doc.fieldOptions.fileName = "FieldOptions.FILENAME.docx";
field.update();

expect(field.getFieldCode()).toEqual(" FILENAME  \\p");
expect(field.result).toEqual("FieldOptions.FILENAME.docx");

doc.updateFields();
doc.save(base.artifactsDir + doc.fieldOptions.fileName);
```

### See Also

* module [Aspose.Words.Fields](../../)
* class [FieldFileName](../)

