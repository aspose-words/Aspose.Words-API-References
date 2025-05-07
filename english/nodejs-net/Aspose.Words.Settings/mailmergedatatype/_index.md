---
title: MailMergeDataType enumeration
linktitle: MailMergeDataType enumeration
articleTitle: MailMergeDataType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Settings.MailMergeDataType enumeration. Specifies the type of an external mail merge data source."
type: docs
weight: 60
url: /nodejs-net/aspose.words.settings/mailmergedatatype/
---

## MailMergeDataType enumeration

Specifies the type of an external mail merge data source.


### Members

| Name | Description |
| --- | --- |
| None | No mail merge data source is specified. |
| TextFile | Specifies that a given document has been connected to a text file via the Dynamic Data Exchange (DDE) system. |
| Database | Specifies that a given document has been connected to an Access database via the Dynamic Data Exchange (DDE) system. |
| Spreadsheet | Specifies that a given document has been connected to an Excel spreadsheet via the Dynamic Data Exchange (DDE) system. |
| Query | Specifies that a given document has been connected to an external data source using an external query tool. |
| Odbc | Specifies that a given document has been connected to an external data source via the Open Database Connectivity interface. |
| Native | Specifies that a given document has been connected to an external data source via the Office Data Source Object (ODSO) interface. |
| Default | Equals to [MailMergeDataType.None](./#None). |

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
* property [MailMergeSettings.dataType](../mailmergesettings/dataType/)

