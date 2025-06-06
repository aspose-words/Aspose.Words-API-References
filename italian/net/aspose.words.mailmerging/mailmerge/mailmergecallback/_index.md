---
title: MailMerge.MailMergeCallback
linktitle: MailMergeCallback
articleTitle: MailMergeCallback
second_title: Aspose.Words per .NET
description: Ottimizza la tua stampa unione con la proprietà MailMergeCallback. Gestisci gli eventi senza sforzo per un'automazione impeccabile dei documenti e una maggiore efficienza.
type: docs
weight: 40
url: /it/net/aspose.words.mailmerging/mailmerge/mailmergecallback/
---
## MailMerge.MailMergeCallback property

Consente di gestire eventi particolari durante la stampa unione.

```csharp
public IMailMergeCallback MailMergeCallback { get; set; }
```

## Esempi

Mostra come definire una logica personalizzata per la gestione degli eventi durante la stampa unione.

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserire due tag di unione di posta che fanno riferimento a due colonne in un'origine dati.
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // Crea un'origine dati che contenga solo una delle colonne a cui fanno riferimento i nostri tag di unione.
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // Configura la nostra stampa unione per utilizzare tag di stampa unione alternativi.
    doc.MailMerge.UseNonMergeFields = true;

    // Quindi, assicurati che la stampa unione converta i tag, come il nostro tag "Cognome",
    // nei MERGEFIELD nei documenti di unione.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// Conta il numero di volte in cui una stampa unione sostituisce i tag di stampa unione che non è riuscita a riempire con i dati tramite MERGEFIELD.
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

### Guarda anche

* interface [IMailMergeCallback](../../imailmergecallback/)
* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
