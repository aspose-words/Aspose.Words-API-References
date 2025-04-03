---
title: MailMergeDestination enumeration
linktitle: MailMergeDestination enumeration
articleTitle: MailMergeDestination enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Settings.MailMergeDestination enumeration. Specifies the possible results which may be generated when a mail merge is carried out on a document."
type: docs
weight: 70
url: /nodejs-net/aspose.words.settings/mailmergedestination/
---

## MailMergeDestination enumeration

Specifies the possible results which may be generated when a mail merge is carried out on a document.


### Members

| Name | Description |
| --- | --- |
| NewDocument | Specifies that conforming hosting applications shall generate new documents by populating the fields within a given document with data from the specified external data source. |
| Printer | Specifies that conforming hosting applications shall print the documents that result from populating the fields within a given document with external data from the specified external data source. |
| Email | Specifies that conforming hosting applications shall generate emails using the documents that result from populating the fields within a given document with data from the specified external data source. |
| Fax | Specifies that conforming hosting applications shall generate faxes using the documents that result from populating the fields within a given document with data from the specified external data source. |
| Default | Equals to the [MailMergeDestination.NewDocument](./#NewDocument) value. |

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

* module [Aspose.Words.Settings](../)
* property [MailMergeSettings.destination](../mailmergesettings/destination/)

