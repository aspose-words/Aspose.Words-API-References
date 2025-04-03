---
title: DocumentBuilder.italic property
linktitle: italic property
articleTitle: italic property
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.italic property. True if the font is formatted as italic."
type: docs
weight: 140
url: /nodejs-net/aspose.words/documentbuilder/italic/
---

## DocumentBuilder.italic property

True if the font is formatted as italic.


```js
get italic(): boolean
```

### Examples

Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
// and then fill them manually.
builder.insertField(" MERGEFIELD Chairman ");
builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.moveToMergeField("Chairman");
builder.bold = true;
builder.writeln("John Doe");

builder.moveToMergeField("ChiefFinancialOfficer");
builder.italic = true;
builder.writeln("Jane Doe");

builder.moveToMergeField("ChiefTechnologyOfficer");
builder.italic = true;
builder.writeln("John Bloggs");

doc.save(base.artifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

