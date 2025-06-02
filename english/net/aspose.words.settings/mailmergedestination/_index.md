---
title: MailMergeDestination Enum
linktitle: MailMergeDestination
articleTitle: MailMergeDestination
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.MailMergeDestination enum, defining outcomes for seamless document mail merges. Optimize your document processing today!
type: docs
weight: 6670
url: /net/aspose.words.settings/mailmergedestination/
---
## MailMergeDestination enumeration

Specifies the possible results which may be generated when a mail merge is carried out on a document.

```csharp
public enum MailMergeDestination
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| NewDocument | `0` | Specifies that conforming hosting applications shall generate new documents by populating the fields within a given document with data from the specified external data source. |
| Printer | `1` | Specifies that conforming hosting applications shall print the documents that result from populating the fields within a given document with external data from the specified external data source. |
| Email | `2` | Specifies that conforming hosting applications shall generate emails using the documents that result from populating the fields within a given document with data from the specified external data source. |
| Fax | `4` | Specifies that conforming hosting applications shall generate faxes using the documents that result from populating the fields within a given document with data from the specified external data source. |
| Default | `0` | Equals to the NewDocument value. |

## Examples

Shows how to execute a mail merge with data from an Office Data Source Object.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// Create a data source in the form of an ASCII file, with the "|" character
// acting as the delimiter that separates columns. The first line contains the three columns' names,
// and each subsequent line is a row with their respective values.
string[] lines = { "FirstName|LastName|Message",
    "John|Doe|Hello! This message was created with Aspose Words mail merge." };
string dataSrcFilename = ArtifactsDir + "MailMerge.MailMergeSettings.DataSource.txt";

File.WriteAllLines(dataSrcFilename, lines);

MailMergeSettings settings = doc.MailMergeSettings;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.CheckErrors = MailMergeCheckErrors.Simulate;
settings.DataType = MailMergeDataType.Native;
settings.DataSource = dataSrcFilename;
settings.Query = "SELECT * FROM " + doc.MailMergeSettings.DataSource;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

Assert.AreEqual(MailMergeDestination.Default, settings.Destination);
Assert.False(settings.DoNotSupressBlankLines);

Odso odso = settings.Odso;
odso.DataSource = dataSrcFilename;
odso.DataSourceType = OdsoDataSourceType.Text;
odso.ColumnDelimiter = '|';
odso.FirstRowContainsColumnNames = true;

Assert.AreNotSame(odso, odso.Clone());
Assert.AreNotSame(settings, settings.Clone());

// Opening this document in Microsoft Word will execute the mail merge before displaying the contents. 
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### See Also

* property [Destination](../mailmergesettings/destination/)
* namespace [Aspose.Words.Settings](../../aspose.words.settings/)
* assembly [Aspose.Words](../../)
