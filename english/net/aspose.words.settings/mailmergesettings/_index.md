---
title: MailMergeSettings Class
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words for .NET
description: Aspose.Words.Settings.MailMergeSettings class. Specifies all of the mail merge information for a document in C#.
type: docs
weight: 6050
url: /net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

Specifies all of the mail merge information for a document.

To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/net/mail-merge-and-reporting/) documentation article.

```csharp
public class MailMergeSettings
```

## Constructors

| Name | Description |
| --- | --- |
| [MailMergeSettings](mailmergesettings/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord/) { get; set; } | Specifies the one-based index of the record from the data source which shall be displayed in Microsoft Word. The default value is 1. |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname/) { get; set; } | Specifies the column within the data source that contains e-mail addresses. The default value is an empty string. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors/) { get; set; } | Specifies the type of error reporting which shall be conducted by Microsoft Word when performing a mail merge. The default value is Default. |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring/) { get; set; } | Specifies the connection string used to connect to an external data source. The default value is an empty string. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource/) { get; set; } | Specifies the path to the mail-merge data source. The default value is an empty string. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype/) { get; set; } | Specifies the type of the mail-merge data source and the method of data access. The default value is Default. |
| [Destination](../../aspose.words.settings/mailmergesettings/destination/) { get; set; } | Specifies how Microsoft Word will output the results of a mail merge. The default value is Default. |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines/) { get; set; } | Specifies how an application performing the mail merge shall handle blank lines in the merged documents resulting from the mail merge. The default value is `false`. |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource/) { get; set; } | Specifies the path to the mail-merge header source. The default value is an empty string. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery/) { get; set; } | Not sure about this one. The Microsoft Word Automation Reference suggests that this specifies that the query is executed every time the document is opened in Microsoft Word. But the OOXML specification suggests that this specifies that the query contains a reference to an external query file which contains the actual query. The default value is `false`. |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment/) { get; set; } | Specifies that the documents produced during a mail merge operation should be emailed as an attachment rather than the body of the actual e-mail. The default value is `false`. |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject/) { get; set; } | Specifies the text which shall appear in the subject line of the e-mails or faxes produced during mail merge. The default value is an empty string. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype/) { get; set; } | Specifies the mail-merge main document type. The default value is Default. |
| [Odso](../../aspose.words.settings/mailmergesettings/odso/) { get; set; } | Gets or sets the object that specifies the Office Data Source Object (ODSO) settings. |
| [Query](../../aspose.words.settings/mailmergesettings/query/) { get; set; } | Contains the Structured Query Language string that shall be run against the specified external data source to return the set of records which shall be imported into the document when the mail merge operation is performed. The default value is an empty string. |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata/) { get; set; } | Specifies that Microsoft Word shall display the data from the specified external data source where merge fields have been inserted (e.g. preview merged data). The default value is `false`. |

## Methods

| Name | Description |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear/)() | Clears the mail merge settings in such a way that when the document is saved, no mail merge settings will be saved and it will become a normal document. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone/)() | Returns a deep clone of this object. |

## Remarks

You can use this object to specify a mail merge data source for a document and this information (along with the available data fields) will appear in Microsoft Word when the user opens this document. Or you can use this object to query mail merge settings that the user has specified in Microsoft Word for this document.

You do not normally need to create objects of this class directly because Mail merge settings of a document are always available via the [`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) property.

To detect whether this document is a mail merge main document, check the value of the [`MainDocumentType`](./maindocumenttype/) property.

To remove mail merge settings and data source information from a document you can use the [`Clear`](./clear/) method. Aspose.Words will not write mail merge settings to a document if the [`MainDocumentType`](./maindocumenttype/) property is set to NotAMergeDocument or the [`DataType`](./datatype/) property is set to None.

The best way to learn how to use the properties of this object is to create a document with a desired data source manually in Microsoft Word and then open that document using Aspose.Words and examine the properties of the [`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) and [`Odso`](./odso/) objects. This is a good approach to take if you want to learn how to programmatically configure a data source, for example.

Aspose.Words preserves mail merge information when loading, saving and converting documents between different formats, but does not use this information when performing its own mail merge using the [`MailMerge`](../../aspose.words.mailmerging/mailmerge/) object.

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
