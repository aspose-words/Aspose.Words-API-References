---
title: IMailMergeCallback Interface
linktitle: IMailMergeCallback
articleTitle: IMailMergeCallback
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihren Serienbriefprozess mit Aspose.Words.MailMerging.IMailMergeCallback. Erhalten Sie Echtzeitbenachrichtigungen und steigern Sie die Effizienz Ihrer Dokumentenautomatisierung.
type: docs
weight: 4490
url: /de/net/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface

Implementieren Sie diese Schnittstelle, wenn Sie während der Serienbriefausführung Benachrichtigungen erhalten möchten.

```csharp
public interface IMailMergeCallback
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [TagsReplaced](../../aspose.words.mailmerging/imailmergecallback/tagsreplaced/)() | Wird aufgerufen, wenn „Mustache“-Text-Tags durch MERGEFIELD-Felder ersetzt werden. |

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

* namensraum [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../)
