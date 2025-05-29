---
title: MailMerge.MergeWholeDocument
linktitle: MergeWholeDocument
articleTitle: MergeWholeDocument
second_title: Aspose.Words per .NET
description: Scopri come la proprietà MailMerge MergeWholeDocument aggiorna tutti i campi durante una stampa unione basata sulla regione, migliorando l'efficienza e la precisione nei tuoi documenti.
type: docs
weight: 70
url: /it/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

Ottiene o imposta un valore che indica se i campi dell'intero documento vengono aggiornati durante l'esecuzione di una stampa unione con regioni.

```csharp
public bool MergeWholeDocument { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` .

## Esempi

Mostra la relazione tra le unioni di posta con le regioni e l'aggiornamento dei campi.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // Se impostiamo il flag "MergeWholeDocument" su "true",
    // la stampa unione con regioni aggiornerà tutti i campi del documento.
    // Se impostiamo il flag "MergeWholeDocument" su "false", la stampa unione aggiornerà solo i campi
    // all'interno dell'area di stampa unione il cui nome corrisponde al nome della tabella di origine dati.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // La stampa unione aggiornerà solo il campo CITAZIONE al di fuori dell'area di stampa unione
    // se impostiamo il flag "MergeWholeDocument" su "true".
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// Crea un documento con un'area di stampa unione che appartiene a un'origine dati denominata "MyTable".
/// Inserire un campo QUOTE all'interno di questa regione e un altro all'esterno.
/// </summary>
private static Document CreateSourceDocMergeWholeDocument()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is outside of the \"MyTable\" merge region.";

    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD TableStart:MyTable");

    field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is inside the \"MyTable\" merge region.";
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD MyColumn");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    return doc;
}

/// <summary>
/// Crea una tabella dati che verrà utilizzata in una stampa unione.
/// </summary>
private static DataTable CreateSourceTableMergeWholeDocument()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("MyColumn");
    dataTable.Rows.Add(new object[] { "MyValue" });

    return dataTable;
}
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
