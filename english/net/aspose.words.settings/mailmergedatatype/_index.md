---
title: MailMergeDataType Enum
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Settings.MailMergeDataType enum. Specifies the type of an external mail merge data source in C#.
type: docs
weight: 5590
url: /net/aspose.words.settings/mailmergedatatype/
---
## MailMergeDataType enumeration

Specifies the type of an external mail merge data source.

```csharp
public enum MailMergeDataType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `-1` | No mail merge data source is specified. |
| TextFile | `0` | Specifies that a given document has been connected to a text file via the Dynamic Data Exchange (DDE) system. |
| Database | `1` | Specifies that a given document has been connected to an Access database via the Dynamic Data Exchange (DDE) system. |
| Spreadsheet | `2` | Specifies that a given document has been connected to an Excel spreadsheet via the Dynamic Data Exchange (DDE) system. |
| Query | `3` | Specifies that a given document has been connected to an external data source using an external query tool. |
| Odbc | `4` | Specifies that a given document has been connected to an external data source via the Open Database Connectivity interface. |
| Native | `5` | Specifies that a given document has been connected to an external data source via the Office Data Source Object (ODSO) interface. |
| Default | `-1` | Equals to None. |

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

* property [DataType](../mailmergesettings/datatype/)
* namespace [Aspose.Words.Settings](../../aspose.words.settings/)
* assembly [Aspose.Words](../../)
