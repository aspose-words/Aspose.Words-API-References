---
title: MappedDataFieldCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: MappedDataFieldCollection Item proprietà. Ottiene o imposta il nome del campo nellorigine dati associata al campo di stampa unione specificato in C#.
type: docs
weight: 20
url: /it/net/aspose.words.mailmerging/mappeddatafieldcollection/item/
---
## MappedDataFieldCollection indexer

Ottiene o imposta il nome del campo nell'origine dati associata al campo di stampa unione specificato.

```csharp
public string this[string documentFieldName] { get; set; }
```

## Esempi

Mostra come mappare colonne di dati e MERGEFIELD con nomi diversi in modo che i dati vengano trasferiti tra loro durante una stampa unione.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // La tabella ha una colonna denominata "Column2", ma non esistono MERGEFIELD con quel nome.
    // Inoltre, abbiamo un MERGEFIELD denominato "Column3", ma l'origine dati non ha una colonna con quel nome.
    // Se i dati della "Colonna2" sono adatti al MERGEFIELD della "Colonna3",
    // possiamo mappare il nome della colonna a MERGEFIELD nella coppia chiave/valore "MappedDataFields".
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Possiamo collegare il nome di una colonna di origine dati a un nome MERGEFIELD come questo.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // Collega la colonna dell'origine dati denominata "Column2" ai MERGEFIELD denominati "Column3".
    mappedDataFields.Add("Column3", "Column2");

    // Il nome MERGEFIELD è la "chiave" per il rispettivo nome "valore" della colonna dell'origine dati.
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Ora se eseguiamo questa stampa unione, i MERGEFIELD "Column3" prenderanno i dati dalla "Column2" della tabella.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    // Possiamo eseguire l'iterazione sugli elementi di questa raccolta.
    Assert.AreEqual(2, mappedDataFields.Count);

    using (IEnumerator<KeyValuePair<string, string>> enumerator = mappedDataFields.GetEnumerator())
        while (enumerator.MoveNext())
            Console.WriteLine(
                $"Column named {enumerator.Current.Value} is mapped to MERGEFIELDs named {enumerator.Current.Key}");

    // Possiamo anche rimuovere elementi dalla raccolta.
    mappedDataFields.Remove("MergeFieldName");

    Assert.False(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.False(mappedDataFields.ContainsValue("DataSourceColumnName"));

    mappedDataFields.Clear();

    Assert.AreEqual(0, mappedDataFields.Count);
}

/// <summary>
/// Crea un documento con 2 MERGEFIELD, uno dei quali non ha un file
/// colonna corrispondente nella tabella dati dal metodo seguente.
/// </summary>
private static Document CreateSourceDocMappedDataFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column3");

    return doc;
}

/// <summary>
/// Crea una tabella dati con 2 colonne, una delle quali non ha un file
/// MERGEFIELD corrispondente nel documento sorgente dal metodo sopra.
/// </summary>
private static DataTable CreateSourceTableMappedDataFields()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value1", "Value2" });

    return dataTable;
}
```

### Guarda anche

* class [MappedDataFieldCollection](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
