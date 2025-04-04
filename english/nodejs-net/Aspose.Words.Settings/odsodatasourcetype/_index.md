---
title: OdsoDataSourceType enumeration
linktitle: OdsoDataSourceType enumeration
articleTitle: OdsoDataSourceType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Settings.OdsoDataSourceType enumeration. Specifies the type of the external data source to be connected to as part of the ODSO connection information."
type: docs
weight: 130
url: /nodejs-net/aspose.words.settings/odsodatasourcetype/
---

## OdsoDataSourceType enumeration

Specifies the type of the external data source to be connected to as part of the ODSO connection information.

The OOXML specification is very vague for this enum. I guess it might correspond to the WdMergeSubType
enumeration http://msdn.microsoft.com/en-us/library/bb237801.aspx.




### Members

| Name | Description |
| --- | --- |
| Text | Specifies that a given document has been connected to a text file. Possibly wdMergeSubTypeOther. |
| Database | Specifies that a given document has been connected to a database. Possibly wdMergeSubTypeAccess. |
| AddressBook | Specifies that a given document has been connected to an address book of contacts. Possibly wdMergeSubTypeOAL. |
| Document1 | Specifies that a given document has been connected to another document format supported by the producing application. Possibly wdMergeSubTypeOLEDBWord. |
| Document2 | Specifies that a given document has been connected to another document format supported by the producing application. Possibly wdMergeSubTypeWorks. |
| Native | Specifies that a given document has been connected to another document format native to the producing application. Possibly wdMergeSubTypeOLEDBText |
| Email | Specifies that a given document has been connected to an e-mail application. Possibly wdMergeSubTypeOutlook. |
| None | The type of the external data source is not specified. Possibly wdMergeSubTypeWord. |
| Legacy | Specifies that a given document has been connected to a legacy document format supported by the producing application  Possibly wdMergeSubTypeWord2000. |
| Master | Specifies that a given document has been connected to a data source which aggregates other data sources. |
| Default | Equals to [OdsoDataSourceType.None](./#None). |

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
* property [Odso.dataSourceType](../odso/dataSourceType/)

