---
title: MailMergeCallback
second_title: Aspose.Words for .NET API Reference
description: MailMerge property. Allows to handle particular events during mail merge in C#.
type: docs
weight: 40
url: /net/aspose.words.mailmerging/mailmerge/mailmergecallback/
---
## MailMerge.MailMergeCallback property

Allows to handle particular events during mail merge.

```csharp
public IMailMergeCallback MailMergeCallback { get; set; }
```

## Examples

Shows how to define custom logic for handling events during mail merge.

```csharp
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

* interface [IMailMergeCallback](../../imailmergecallback/)
* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../mailmerge/)
* assembly [Aspose.Words](../../../)
