---
title: MailMergeSettings.MainDocumentType
linktitle: MainDocumentType
articleTitle: MainDocumentType
second_title: Aspose.Words for .NET
description: Discover how the MailMergeSettings MainDocumentType property defines your mail merge documents. Unlock seamless document creation with optimal settings!
type: docs
weight: 140
url: /net/aspose.words.settings/mailmergesettings/maindocumenttype/
---
## MailMergeSettings.MainDocumentType property

Specifies the mail-merge main document type. The default value is Default.

```csharp
public MailMergeMainDocumentType MainDocumentType { get; set; }
```

## Remarks

The main document is the document that contains information that is the same for each version of the merged document.

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

Assert.That(settings.Destination, Is.EqualTo(MailMergeDestination.Default));
Assert.That(settings.DoNotSupressBlankLines, Is.False);

Odso odso = settings.Odso;
odso.DataSource = dataSrcFilename;
odso.DataSourceType = OdsoDataSourceType.Text;
odso.ColumnDelimiter = '|';
odso.FirstRowContainsColumnNames = true;

Assert.That(odso.Clone(), Is.Not.SameAs(odso));
Assert.That(settings.Clone(), Is.Not.SameAs(settings));

// Opening this document in Microsoft Word will execute the mail merge before displaying the contents. 
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### See Also

* enum [MailMergeMainDocumentType](../../mailmergemaindocumenttype/)
* class [MailMergeSettings](../)
* namespace [Aspose.Words.Settings](../../../aspose.words.settings/)
* assembly [Aspose.Words](../../../)
