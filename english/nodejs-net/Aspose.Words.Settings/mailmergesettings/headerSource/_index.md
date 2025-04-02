---
title: MailMergeSettings.headerSource property
linktitle: headerSource property
articleTitle: headerSource property
second_title: Aspose.Words for NodeJs
description: "MailMergeSettings.headerSource property. Specifies the path to the mail-merge header source"
type: docs
weight: 100
url: /nodejs-net/Aspose.Words.Settings/mailmergesettings/headerSource/
---

## MailMergeSettings.headerSource property

Specifies the path to the mail-merge header source.
The default value is an empty string.


```js
get headerSource(): string
```

### Examples

Shows how to construct a data source for a mail merge from a header source and a data source.

```js
// Create a mailing label merge header file, which will consist of a table with one row.
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.startTable();
builder.insertCell();
builder.write("FirstName");
builder.insertCell();
builder.write("LastName");
builder.endTable();

doc.save(base.artifactsDir + "MailMerge.MailingLabelMerge.header.docx");

// Create a mailing label merge data file consisting of a table with one row
// and the same number of columns as the header document's table. 
doc = new aw.Document();
builder = new aw.DocumentBuilder(doc);

builder.startTable();
builder.insertCell();
builder.write("John");
builder.insertCell();
builder.write("Doe");
builder.endTable();

doc.save(base.artifactsDir + "MailMerge.MailingLabelMerge.data.docx");

// Create a merge destination document with MERGEFIELDS with names that
// match the column names in the merge header file table.
doc = new aw.Document();
builder = new aw.DocumentBuilder(doc);

builder.write("Dear ");
builder.insertField("MERGEFIELD FirstName", "<FirstName>");
builder.write(" ");
builder.insertField("MERGEFIELD LastName", "<LastName>");

let settings = doc.mailMergeSettings;

// Construct a data source for our mail merge by specifying two document filenames.
// The header source will name the columns of the data source table.
settings.headerSource = base.artifactsDir + "MailMerge.MailingLabelMerge.header.docx";

// The data source will provide rows of data for all the columns in the header document table.
settings.dataSource = base.artifactsDir + "MailMerge.MailingLabelMerge.data.docx";

// Configure a mailing label type mail merge, which Microsoft Word will execute
// as soon as we use it to load the output document.
settings.query = "SELECT * FROM " + settings.dataSource;
settings.mainDocumentType = aw.Settings.MailMergeMainDocumentType.MailingLabels;
settings.dataType = aw.Settings.MailMergeDataType.TextFile;
settings.linkToQuery = true;
settings.viewMergedData = true;

doc.save(base.artifactsDir + "MailMerge.MailingLabelMerge.docx");
```

### See Also

* module [Aspose.Words.Settings](../../)
* class [MailMergeSettings](../)

