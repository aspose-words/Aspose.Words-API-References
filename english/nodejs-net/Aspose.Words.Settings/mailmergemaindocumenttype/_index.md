---
title: MailMergeMainDocumentType enumeration
linktitle: MailMergeMainDocumentType enumeration
articleTitle: MailMergeMainDocumentType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Settings.MailMergeMainDocumentType enumeration. Specifies the possible types for a mail merge source document."
type: docs
weight: 80
url: /nodejs-net/aspose.words.settings/mailmergemaindocumenttype/
---

## MailMergeMainDocumentType enumeration

Specifies the possible types for a mail merge source document.


### Members

| Name | Description |
| --- | --- |
| NotAMergeDocument | This document is not a mail merge document. |
| FormLetters | Specifies that the mail merge source document is of the form letter type. |
| MailingLabels | Specifies that the mail merge source document is of the mailing label type. |
| Envelopes | Specifies that the mail merge source document is of the envelope type. |
| Catalog | Specifies that the mail merge source document is of the catalog type. |
| Email | Specifies that the mail merge source document is of the e-mail message type. |
| Fax | Specifies that the mail merge source document is of the fax type. |
| Default | Equals to [MailMergeMainDocumentType.NotAMergeDocument](./#NotAMergeDocument) |

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
* property [MailMergeSettings.mainDocumentType](../mailmergesettings/mainDocumentType/)

