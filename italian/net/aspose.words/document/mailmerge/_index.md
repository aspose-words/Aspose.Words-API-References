---
title: Document.MailMerge
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words per .NET
description: Sblocca l'automazione perfetta dei documenti con l'oggetto MailMerge, migliorando il flusso di lavoro semplificando senza sforzo le attività di unione della posta.
type: docs
weight: 270
url: /it/net/aspose.words/document/mailmerge/
---
## Document.MailMerge property

Restituisce un[`MailMerge`](../../../aspose.words.mailmerging/mailmerge/) oggetto che rappresenta la funzionalità di unione di posta per il documento.

```csharp
public MailMerge MailMerge { get; }
```

## Esempi

Mostra come eseguire una stampa unione con i dati di una DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Di seguito sono riportati due modi per utilizzare una DataTable come origine dati per una stampa unione.
    // 1 - Utilizza l'intera tabella per la stampa unione per creare un documento di stampa unione in output per ogni riga della tabella:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilizzare una riga della tabella per creare un documento di stampa unione in output:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento sorgente per la stampa unione.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Guarda anche

* class [MailMerge](../../../aspose.words.mailmerging/mailmerge/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
