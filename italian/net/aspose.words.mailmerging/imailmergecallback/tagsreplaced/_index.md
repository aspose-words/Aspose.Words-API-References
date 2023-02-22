---
title: IMailMergeCallback.TagsReplaced
second_title: Aspose.Words per .NET API Reference
description: IMailMergeCallback metodo. Chiamato quando i tag di testo baffi vengono sostituiti con i campi MERGEFIELD.
type: docs
weight: 10
url: /it/net/aspose.words.mailmerging/imailmergecallback/tagsreplaced/
---
## IMailMergeCallback.TagsReplaced method

Chiamato quando i tag di testo "baffi" vengono sostituiti con i campi MERGEFIELD.

```csharp
public void TagsReplaced()
```

### Esempi

Mostra come definire una logica personalizzata per la gestione degli eventi durante la stampa unione.

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserisce due tag di stampa unione che fanno riferimento a due colonne in un'origine dati.
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
    // in MERGEFIELD nei documenti di unione.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// Conta il numero di volte in cui una stampa unione sostituisce i tag di stampa unione che non poteva riempire con i dati con MERGEFIELD.
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

* property [UseNonMergeFields](../../mailmerge/usenonmergefields/)
* interface [IMailMergeCallback](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../imailmergecallback/)
* assemblea [Aspose.Words](../../../)


