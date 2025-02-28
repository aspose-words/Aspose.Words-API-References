---
title: IMailMergeCallback Interface
linktitle: IMailMergeCallback
articleTitle: IMailMergeCallback
second_title: Aspose.Words for .NET
description: Optimize your mail merge process with Aspose.Words.MailMerging.IMailMergeCallback. Get real-time notifications and enhance your document automation efficiency.
type: docs
weight: 4360
url: /net/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface

Implement this interface if you want to receive notifications while mail merge is performed.

```csharp
public interface IMailMergeCallback
```

## Methods

| Name | Description |
| --- | --- |
| [TagsReplaced](../../aspose.words.mailmerging/imailmergecallback/tagsreplaced/)() | Called when "mustache" text tags are replaced with MERGEFIELD fields. |

## Examples

Shows how to define custom logic for handling events during mail merge.

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insert two mail merge tags referencing two columns in a data source.
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // Create a data source that only contains one of the columns that our merge tags reference.
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // Configure our mail merge to use alternative mail merge tags.
    doc.MailMerge.UseNonMergeFields = true;

    // Then, ensure that the mail merge will convert tags, such as our "LastName" tag,
    // into MERGEFIELDs in the merge documents.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// Counts the number of times a mail merge replaces mail merge tags that it could not fill with data with MERGEFIELDs.
/// </summary>
private class MailMergeTagReplacementCounter : IMailMergeCallback
{
    public void TagsReplaced()
    {
        TagsReplacedCount++;
    }

    public int TagsReplacedCount { get; private set; }
}
```

### See Also

* namespace [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../)
