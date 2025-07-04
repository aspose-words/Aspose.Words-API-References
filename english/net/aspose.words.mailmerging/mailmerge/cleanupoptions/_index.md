---
title: MailMerge.CleanupOptions
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: Aspose.Words for .NET
description: Optimize your mail merge with the CleanupOptions property—easily manage which items to remove for a seamless, efficient process.
type: docs
weight: 10
url: /net/aspose.words.mailmerging/mailmerge/cleanupoptions/
---
## MailMerge.CleanupOptions property

Gets or sets a set of flags that specify what items should be removed during mail merge.

```csharp
public MailMergeCleanupOptions CleanupOptions { get; set; }
```

## Examples

Shows how to remove empty paragraphs that a mail merge may create from the merge output document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD TableStart:MyTable");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertField(" MERGEFIELD TableEnd:MyTable");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.ExecuteWithRegions(dataTable);

if (doc.MailMerge.CleanupOptions == MailMergeCleanupOptions.RemoveEmptyParagraphs) 
    Assert.That(doc.GetText().Trim(), Is.EqualTo("John Doe\r" +
        "Jane Doe"));
else
    Assert.That(doc.GetText().Trim(), Is.EqualTo("John Doe\r" +
        " \r" +
        "Jane Doe"));
```

Shows how to automatically remove MERGEFIELDs that go unused during mail merge.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a document with MERGEFIELDs for three columns of a mail merge data source table,
// and then create a table with only two columns whose names match our MERGEFIELDs.
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs" });

// Our third MERGEFIELD references a "City" column, which does not exist in our data source.
// The mail merge will leave fields such as this intact in their pre-merge state.
// Setting the "CleanupOptions" property to "RemoveUnusedFields" will remove any MERGEFIELDs
// that go unused during a mail merge to clean up the merge documents.
doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.Execute(dataTable);

if (mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveUnusedFields || 
    mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveStaticFields)
    Assert.That(doc.Range.Fields.Count, Is.EqualTo(0));
else
    Assert.That(doc.Range.Fields.Count, Is.EqualTo(2));
```

### See Also

* enum [MailMergeCleanupOptions](../../mailmergecleanupoptions/)
* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
