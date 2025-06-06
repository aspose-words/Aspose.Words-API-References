---
title: IMailMergeCallback Interface
linktitle: IMailMergeCallback
articleTitle: IMailMergeCallback
second_title: Aspose.Words per .NET
description: Ottimizza il tuo processo di stampa unione con Aspose.Words.MailMerging.IMailMergeCallback. Ricevi notifiche in tempo reale e migliora l'efficienza dell'automazione dei tuoi documenti.
type: docs
weight: 4490
url: /it/net/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface

Implementa questa interfaccia se vuoi ricevere notifiche mentre viene eseguita la stampa unione.

```csharp
public interface IMailMergeCallback
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [TagsReplaced](../../aspose.words.mailmerging/imailmergecallback/tagsreplaced/)() | Chiamato quando i tag di testo "baffi" vengono sostituiti con campi MERGEFIELD. |

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

* spazio dei nomi [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../)
