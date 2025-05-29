---
title: MailMerge.UseWholeParagraphAsRegion
linktitle: UseWholeParagraphAsRegion
articleTitle: UseWholeParagraphAsRegion
second_title: Aspose.Words per .NET
description: Scopri come utilizzare la proprietà UseWholeParagraphAsRegion di MailMerge per migliorare le aree di stampa unione, garantendo il controllo completo sull'inclusione dei contenuti.
type: docs
weight: 160
url: /it/net/aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/
---
## MailMerge.UseWholeParagraphAsRegion property

Ottiene o imposta un valore che indica se l'intero paragrafo con**TableStart** O**TableEnd** field o intervallo particolare tra**TableStart** E**TableEnd** i campi dovrebbero essere inclusi nell'area di unione della stampa.

```csharp
public bool UseWholeParagraphAsRegion { get; set; }
```

## Osservazioni

Il valore predefinito è`VERO` .

## Esempi

Mostra la relazione tra le aree di stampa unione e i paragrafi.

```csharp
public void UseWholeParagraphAsRegion(bool useWholeParagraphAsRegion)
{
    Document doc = CreateSourceDocWithNestedMergeRegions();
    DataTable dataTable = CreateSourceTableDataTableForOneRegion();

    // Per impostazione predefinita, un paragrafo non può appartenere a più di un'area di stampa unione.
    // Il contenuto del nostro documento non soddisfa questi criteri.
    // Se impostiamo il flag "UseWholeParagraphAsRegion" su "true",
    // l'esecuzione di una stampa unione su questo documento genererà un'eccezione.
    // Se impostiamo il flag "UseWholeParagraphAsRegion" su "false",
    // saremo in grado di eseguire una stampa unione su questo documento.
    doc.MailMerge.UseWholeParagraphAsRegion = useWholeParagraphAsRegion;

    if (useWholeParagraphAsRegion)
        Assert.Throws<InvalidOperationException>(() => doc.MailMerge.ExecuteWithRegions(dataTable));
    else
        doc.MailMerge.ExecuteWithRegions(dataTable);

    // La stampa unione popola la nostra prima regione lasciando inutilizzata la seconda regione
    // poiché è la regione che infrange la regola.
    doc.Save(ArtifactsDir + "MailMerge.UseWholeParagraphAsRegion.docx");
}

/// <summary>
/// Crea un documento con due aree di stampa unione che condividono un paragrafo.
/// </summary>
private static Document CreateSourceDocWithNestedMergeRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Region 1: ");
    builder.InsertField(" MERGEFIELD TableStart:MyTable");
    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    builder.Write(", Region 2: ");
    builder.InsertField(" MERGEFIELD TableStart:MyOtherTable");
    builder.InsertField(" MERGEFIELD TableEnd:MyOtherTable");

    return doc;
}

/// <summary>
/// Creare una tabella dati che possa popolare una regione durante una stampa unione.
/// </summary>
private static DataTable CreateSourceTableDataTableForOneRegion()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value 1", "Value 2" });

    return dataTable;
}
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
