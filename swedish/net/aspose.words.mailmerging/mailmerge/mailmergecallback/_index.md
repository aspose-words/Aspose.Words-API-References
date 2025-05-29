---
title: MailMerge.MailMergeCallback
linktitle: MailMergeCallback
articleTitle: MailMergeCallback
second_title: Aspose.Words för .NET
description: Optimera din dokumentkoppling med egenskapen MailMergeCallback. Hantera händelser enkelt för sömlös dokumentautomation och förbättrad effektivitet.
type: docs
weight: 40
url: /sv/net/aspose.words.mailmerging/mailmerge/mailmergecallback/
---
## MailMerge.MailMergeCallback property

Tillåter hantering av specifika händelser under dokumentkoppling.

```csharp
public IMailMergeCallback MailMergeCallback { get; set; }
```

## Exempel

Visar hur man definierar anpassad logik för hantering av händelser under dokumentkoppling.

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Infoga två kopplingstaggar som refererar till två kolumner i en datakälla.
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // Skapa en datakälla som bara innehåller en av de kolumner som våra merge-taggar refererar till.
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // Konfigurera vår dokumentkoppling för att använda alternativa taggar för dokumentkoppling.
    doc.MailMerge.UseNonMergeFields = true;

    // Se sedan till att dokumentkopplingen konverterar taggar, till exempel vår "LastName"-tagg,
    // i MERGEFIELDS i merge-dokumenten.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// Räknar antalet gånger en dokumentkoppling ersätter dokumentkopplingstaggar som den inte kunde fylla med data med MERGEFIELDS.
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

### Se även

* interface [IMailMergeCallback](../../imailmergecallback/)
* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
