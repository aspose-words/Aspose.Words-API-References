---
title: Odso Class
linktitle: Odso
articleTitle: Odso
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Settings.Odso class for seamless mail merge integration. Optimize your ODSO settings for efficient data source management.
type: docs
weight: 6710
url: /net/aspose.words.settings/odso/
---
## Odso class

Specifies the Office Data Source Object (ODSO) settings for a mail merge data source.

To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/net/mail-merge-and-reporting/) documentation article.

```csharp
public class Odso
```

## Constructors

| Name | Description |
| --- | --- |
| [Odso](odso/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | Specifies the character which shall be interpreted as the column delimiter used to separate columns within external data sources. The default value is 0 which means there is no column delimiter defined. |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | Specifies the location of the external data source to be connected to a document to perform the mail merge. The default value is an empty string. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | Specifies the type of the external data source to be connected to as part of the ODSO connection information for this mail merge. The default value is Default. |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | Gets or sets a collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document. This object is never `null`. |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | Specifies that a hosting application shall treat the first row of data in the specified external data source as a header row containing the names of each column in the data source. The default value is `false`. |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | Gets or sets a collection of objects that specify inclusion/exclusion of individual records in the mail merge. This object is never `null`. |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | Specifies the particular set of data that a source shall be connected to within an external data source. The default value is an empty string. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | Specifies the Universal Data Link (UDL) connection string used to connect to an external data source. The default value is an empty string. |

## Methods

| Name | Description |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | Returns a deep clone of this object. |

## Remarks

ODSO seems to be the "new" way the newer Microsoft Word versions prefer to use when specifying certain types of data sources for a mail merge document. ODSO probably first appeared in Microsoft Word 2000.

The use of ODSO is poorly documented and the best way to learn how to use the properties of this object is to create a document with a desired data source manually in Microsoft Word and then open that document using Aspose.Words and examine the properties of the [`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) and [`Odso`](../mailmergesettings/odso/) objects. This is a good approach to take if you want to learn how to programmatically configure a data source, for example.

You do not normally need to create objects of this class directly because ODSO settings are always available via the [`Odso`](../mailmergesettings/odso/) property.

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

* namespace [Aspose.Words.Settings](../../aspose.words.settings/)
* assembly [Aspose.Words](../../)
