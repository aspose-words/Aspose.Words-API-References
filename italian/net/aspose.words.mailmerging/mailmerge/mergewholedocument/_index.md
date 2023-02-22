---
title: MailMerge.MergeWholeDocument
second_title: Aspose.Words per .NET API Reference
description: MailMerge proprietà. Ottiene o imposta un valore che indica se i campi dellintero documento vengono aggiornati durante lesecuzione di una stampa unione con le regioni.
type: docs
weight: 70
url: /it/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

Ottiene o imposta un valore che indica se i campi dell'intero documento vengono aggiornati durante l'esecuzione di una stampa unione con le regioni.

```csharp
public bool MergeWholeDocument { get; set; }
```

### Osservazioni

Il valore predefinito è **falso** .

### Esempi

Mostra la relazione tra la stampa unione con le aree geografiche e l'aggiornamento dei campi.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // Se impostiamo il flag "MergeWholeDocument" su "true",
    // la stampa unione con le regioni aggiornerà tutti i campi del documento.
    // Se impostiamo il flag "MergeWholeDocument" su "false", la stampa unione aggiornerà solo i campi
    // all'interno dell'area della stampa unione il cui nome corrisponde al nome della tabella dell'origine dati.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // La stampa unione aggiornerà solo il campo QUOTE al di fuori dell'area della stampa unione
    // se impostiamo il flag "MergeWholeDocument" su "true".
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// Crea un documento con una regione di stampa unione che appartiene a un'origine dati denominata "MyTable".
/// Inserisci un campo QUOTE all'interno di questa regione e un altro al di fuori di essa.
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
/// Crea una tabella di dati che verrà utilizzata in una stampa unione.
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
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)


