---
title: MailMerge.MergeDuplicateRegions
second_title: Aspose.Words per .NET API Reference
description: MailMerge proprietà. Ottiene o imposta un valore che indica se tutte le aree di stampa unione del documento con il nome di unorigine dati devono essere unite durante lesecuzione di una stampa unione con aree rispetto allorigine dati o solo la prima.
type: docs
weight: 60
url: /it/net/aspose.words.mailmerging/mailmerge/mergeduplicateregions/
---
## MailMerge.MergeDuplicateRegions property

Ottiene o imposta un valore che indica se tutte le aree di stampa unione del documento con il nome di un'origine dati devono essere unite durante l'esecuzione di una stampa unione con aree rispetto all'origine dati o solo la prima.

```csharp
public bool MergeDuplicateRegions { get; set; }
```

### Osservazioni

Il valore predefinito è`falso` .

### Esempi

Mostra come lavorare con aree di stampa unione duplicate.

```csharp
public void MergeDuplicateRegions(bool mergeDuplicateRegions)
{
    Document doc = CreateSourceDocMergeDuplicateRegions();
    DataTable dataTable = CreateSourceTableMergeDuplicateRegions();

    // Se impostiamo la proprietà "MergeDuplicateRegions" su "false", la stampa unione interesserà la prima regione,
    // mentre i MERGEFIELD del secondo verranno lasciati nello stato di pre-unione.
    // Per unire entrambe le regioni in questo modo,
    // dovremmo eseguire la stampa unione due volte su una tabella con lo stesso nome.
    // Se impostiamo la proprietà "MergeDuplicateRegions" su "true", la stampa unione interesserà entrambe le regioni.
    doc.MailMerge.MergeDuplicateRegions = mergeDuplicateRegions;

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMerge.MergeDuplicateRegions.docx");
}

/// <summary>
/// Restituisce un documento che contiene due regioni di stampa unione duplicate (che condividono lo stesso nome nei tag "TableStart/End").
/// </summary>
private static Document CreateSourceDocMergeDuplicateRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column1");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");

    return doc;
}

/// <summary>
/// Crea una tabella dati con una riga e due colonne.
/// </summary>
private static DataTable CreateSourceTableMergeDuplicateRegions()
{
    DataTable dataTable = new DataTable("MergeRegion");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value 1", "Value 2" });

    return dataTable;
}
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)


