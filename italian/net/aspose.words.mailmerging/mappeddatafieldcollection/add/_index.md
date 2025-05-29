---
title: MappedDataFieldCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words per .NET
description: Scopri come utilizzare il metodo Add di MappedDataFieldCollection per creare senza sforzo nuove mappature dei campi e migliorare l'efficienza della gestione dei dati.
type: docs
weight: 30
url: /it/net/aspose.words.mailmerging/mappeddatafieldcollection/add/
---
## MappedDataFieldCollection.Add method

Aggiunge una nuova mappatura dei campi.

```csharp
public void Add(string documentFieldName, string dataSourceFieldName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| documentFieldName | String | Nome con distinzione tra maiuscole e minuscole del campo di stampa unione nel documento. |
| dataSourceFieldName | String | Nome del campo nell'origine dati, con distinzione tra maiuscole e minuscole. |

## Esempi

Mostra come mappare colonne di dati e MERGEFIELD con nomi diversi in modo che i dati vengano trasferiti tra di essi durante una stampa unione.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // La tabella ha una colonna denominata "Column2", ma non ci sono MERGEFIELD con quel nome.
    // Inoltre, abbiamo un MERGEFIELD denominato "Column3", ma l'origine dati non ha una colonna con quel nome.
    // Se i dati di "Colonna2" sono adatti per il MERGEFIELD di "Colonna3",
    // possiamo mappare il nome di quella colonna al MERGEFIELD nella coppia chiave/valore "MappedDataFields".
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Possiamo collegare il nome di una colonna di un'origine dati a un nome MERGEFIELD in questo modo.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // Collega la colonna di origine dati denominata "Colonna2" ai MERGEFIELD denominati "Colonna3".
    mappedDataFields.Add("Column3", "Column2");

    // Il nome MERGEFIELD è la "chiave" per il nome "valore" della colonna della rispettiva origine dati.
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Ora, se eseguiamo questa stampa unione, i MERGEFIELD "Column3" prenderanno i dati da "Column2" della tabella.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    // Possiamo scorrere gli elementi di questa raccolta.
    Assert.AreEqual(2, mappedDataFields.Count);

    using (IEnumerator<KeyValuePair<string, string>> enumerator = mappedDataFields.GetEnumerator())
        while (enumerator.MoveNext())
            Console.WriteLine(
                $"Column named {enumerator.Current.Value} is mapped to MERGEFIELDs named {enumerator.Current.Key}");

    // Possiamo anche rimuovere elementi dalla collezione.
    mappedDataFields.Remove("MergeFieldName");

    Assert.False(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.False(mappedDataFields.ContainsValue("DataSourceColumnName"));

    mappedDataFields.Clear();

    Assert.AreEqual(0, mappedDataFields.Count);
}

/// <summary>
/// Crea un documento con 2 MERGEFIELD, uno dei quali non ha un
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
/// Crea una tabella dati con 2 colonne, una delle quali non ha un
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
