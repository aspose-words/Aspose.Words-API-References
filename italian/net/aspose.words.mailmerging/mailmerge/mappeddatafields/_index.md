---
title: MailMerge.MappedDataFields
second_title: Aspose.Words per .NET API Reference
description: MailMerge proprietà. Restituisce una raccolta che rappresenta i campi di dati mappati per loperazione di stampa unione.
type: docs
weight: 50
url: /it/net/aspose.words.mailmerging/mailmerge/mappeddatafields/
---
## MailMerge.MappedDataFields property

Restituisce una raccolta che rappresenta i campi di dati mappati per l'operazione di stampa unione.

```csharp
public MappedDataFieldCollection MappedDataFields { get; }
```

### Osservazioni

I campi di dati mappati consentono di mappare automaticamente tra i nomi dei campi nell'origine dati e i nomi dei campi di stampa unione nel documento.

### Esempi

Mostra come mappare colonne di dati e MERGEFIELD con nomi diversi in modo che i dati vengano trasferiti tra di loro durante una stampa unione.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // La tabella ha una colonna denominata "Colonna2", ma non ci sono MERGEFIELD con quel nome.
    // Inoltre, abbiamo un MERGEFIELD chiamato "Column3", ma l'origine dati non ha una colonna con quel nome.
    // Se i dati di "Column2" sono adatti per MERGEFIELD "Column3",
    // possiamo mappare il nome della colonna al MERGEFIELD nella coppia chiave/valore "MappedDataFields".
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Possiamo collegare il nome di una colonna di un'origine dati a un nome MERGEFIELD come questo.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // Collega la colonna dell'origine dati denominata "Column2" a MERGEFIELD denominati "Column3".
    mappedDataFields.Add("Column3", "Column2");

    // Il nome MERGEFIELD è la "chiave" del nome "valore" della colonna dell'origine dati corrispondente.
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Ora, se eseguiamo questa stampa unione, i MERGEFIELD "Column3" prenderanno i dati da "Column2" della tabella.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    // Possiamo scorrere gli elementi in questa raccolta.
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
/// Crea un documento con 2 MERGEFIELD, uno dei quali non ha a
/// colonna corrispondente nella tabella dei dati dal metodo seguente.
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
/// Crea una tabella dati con 2 colonne, una delle quali non ha a
/// MERGEFIELD corrispondente nel documento di origine dal metodo sopra.
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

* class [MappedDataFieldCollection](../../mappeddatafieldcollection/)
* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmerge/)
* assemblea [Aspose.Words](../../../)


