---
title: MailMerge.MailMergeCallback
linktitle: MailMergeCallback
articleTitle: MailMergeCallback
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihren Serienbrief mit der MailMergeCallback-Eigenschaft. Verwalten Sie Ereignisse mühelos für eine nahtlose Dokumentenautomatisierung und mehr Effizienz.
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

Zeigt, wie Sie eine benutzerdefinierte Logik für die Ereignisbehandlung während des Seriendrucks definieren.

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Fügen Sie zwei Serienbrief-Tags ein, die auf zwei Spalten in einer Datenquelle verweisen.
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // Erstellen Sie eine Datenquelle, die nur eine der Spalten enthält, auf die unsere Merge-Tags verweisen.
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // Konfigurieren Sie unseren Serienbrief so, dass alternative Serienbrief-Tags verwendet werden.
    doc.MailMerge.UseNonMergeFields = true;

    // Stellen Sie dann sicher, dass der Serienbrief Tags konvertiert, wie z. B. unseren Tag „Nachname“,
    // in MERGEFIELDs in den Merge-Dokumenten.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// Zählt, wie oft ein Serienbrief Serienbrief-Tags ersetzt, die er nicht mit Daten durch MERGEFIELDs füllen konnte.
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
