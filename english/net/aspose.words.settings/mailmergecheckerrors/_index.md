---
title: MailMergeCheckErrors Enum
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Settings.MailMergeCheckErrors enum. Specifies how Microsoft Word will report errors detected during mail merge in C#.
type: docs
weight: 5580
url: /net/aspose.words.settings/mailmergecheckerrors/
---
## MailMergeCheckErrors enumeration

Specifies how Microsoft Word will report errors detected during mail merge.

```csharp
public enum MailMergeCheckErrors
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Simulate | `1` | Simulate the merge and report errors in a new document. |
| PauseOnError | `2` | Complete the merge and pause to report errors. |
| CollectErrors | `3` | Complete the merge and report errors in a new document. |
| Default | `2` | Equals to the PauseOnError value. |

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

* property [CheckErrors](../mailmergesettings/checkerrors/)
* namespace [Aspose.Words.Settings](../../aspose.words.settings/)
* assembly [Aspose.Words](../../)
