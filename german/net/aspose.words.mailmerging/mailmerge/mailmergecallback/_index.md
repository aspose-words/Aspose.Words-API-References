---
title: MailMerge.MailMergeCallback
linktitle: MailMergeCallback
articleTitle: MailMergeCallback
second_title: Aspose.Words für .NET
description: MailMerge MailMergeCallback eigendom. Ermöglicht die Verarbeitung bestimmter Ereignisse während des Seriendrucks in C#.
type: docs
weight: 40
url: /de/net/aspose.words.mailmerging/mailmerge/mailmergecallback/
---
## MailMerge.MailMergeCallback property

Ermöglicht die Verarbeitung bestimmter Ereignisse während des Seriendrucks.

```csharp
public IMailMergeCallback MailMergeCallback { get; set; }
```

## Beispiele

Zeigt, wie Sie benutzerdefinierte Logik für die Verarbeitung von Ereignissen während des Seriendrucks definieren.

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Zwei Serienbrief-Tags einfügen, die auf zwei Spalten in einer Datenquelle verweisen.
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // Erstellen Sie eine Datenquelle, die nur eine der Spalten enthält, auf die unsere Merge-Tags verweisen.
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // Konfigurieren Sie unseren Serienbrief, um alternative Serienbrief-Tags zu verwenden.
    doc.MailMerge.UseNonMergeFields = true;

    // Stellen Sie dann sicher, dass der Serienbrief Tags konvertiert, z. B. unser „LastName“-Tag.
    // in MERGEFIELDs in den Zusammenführungsdokumenten.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// Zählt, wie oft ein Serienbrief Serienbrief-Tags ersetzt, die nicht mit Daten mit MERGEFIELDs gefüllt werden konnten.
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

### Siehe auch

* interface [IMailMergeCallback](../../imailmergecallback/)
* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
