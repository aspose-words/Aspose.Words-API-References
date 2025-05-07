---
title: Document.mailMergeSettings property
linktitle: mailMergeSettings property
articleTitle: mailMergeSettings property
second_title: Aspose.Words for Node.js
description: "Document.mailMergeSettings property. Gets or sets the object that contains all of the mail merge information for a document."
type: docs
weight: 270
url: /nodejs-net/aspose.words/document/mailMergeSettings/
---

## Document.mailMergeSettings property

Gets or sets the object that contains all of the mail merge information for a document.


```js
get mailMergeSettings(): Aspose.Words.Settings.MailMergeSettings
```

### Remarks

You can use this object to specify a mail merge data source for a document and this information
(along with the available data fields) will appear in Microsoft Word when the user opens this document.
Or you can use this object to query mail merge settings that the user has specified in Microsoft Word
for this document.

This object is never ``null``.




### Examples

Shows how to execute a mail merge with data from an Office Data Source Object.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Dear ");
builder.insertField("MERGEFIELD FirstName", "<FirstName>");
builder.write(" ");
builder.insertField("MERGEFIELD LastName", "<LastName>");
builder.writeln(": ");
builder.insertField("MERGEFIELD Message", "<Message>");

// Create a data source in the form of an ASCII file, with the "|" character
// acting as the delimiter that separates columns. The first line contains the three columns' names,
// and each subsequent line is a row with their respective values.
string[] lines = { "FirstName|LastName|Message",
  "John|Doe|Hello! This message was created with Aspose Words mail merge." };
string dataSrcFilename = base.artifactsDir + "MailMerge.mailMergeSettings.dataSource.txt";

File.WriteAllLines(dataSrcFilename, lines);

let settings = doc.mailMergeSettings;
settings.mainDocumentType = aw.Settings.MailMergeMainDocumentType.MailingLabels;
settings.checkErrors = aw.Settings.MailMergeCheckErrors.Simulate;
settings.dataType = aw.Settings.MailMergeDataType.Native;
settings.dataSource = dataSrcFilename;
settings.query = "SELECT * FROM " + doc.mailMergeSettings.dataSource;
settings.linkToQuery = true;
settings.viewMergedData = true;

expect(settings.destination).toEqual(aw.Settings.MailMergeDestination.Default);
expect(settings.doNotSupressBlankLines).toEqual(false);

let odso = settings.odso;
odso.dataSource = dataSrcFilename;
odso.dataSourceType = aw.Settings.OdsoDataSourceType.Text;
odso.columnDelimiter = '|';
odso.firstRowContainsColumnNames = true;

Assert.AreNotSame(odso, odso.clone());
Assert.AreNotSame(settings, settings.clone());

// Opening this document in Microsoft Word will execute the mail merge before displaying the contents. 
doc.save(base.artifactsDir + "MailMerge.mailMergeSettings.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

