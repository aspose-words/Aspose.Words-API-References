---
title: MoveToMergeField
second_title: Aspose.Words per .NET API Reference
description: Sposta il cursore in una posizione appena oltre il campo di unione specificato e rimuove il campo di unione.
type: docs
weight: 530
url: /it/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(string) {#movetomergefield}

Sposta il cursore in una posizione appena oltre il campo di unione specificato e rimuove il campo di unione.

```csharp
public bool MoveToMergeField(string fieldName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldName | String | Il nome senza distinzione tra maiuscole e minuscole del campo della stampa unione. |

### Valore di ritorno

True se il campo di unione è stato trovato e il cursore è stato spostato; falso altrimenti.

### Osservazioni

Si noti che questo metodo elimina il campo di unione dal documento dopo aver spostato il cursore.

### Esempi

Mostra come riempire MERGEFIELD con i dati con un generatore di documenti invece di una stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce alcuni MERGEFIELDS, che accettano dati da colonne con lo stesso nome in un'origine dati durante una stampa unione,
// e poi riempili manualmente.
builder.InsertField(" MERGEFIELD Chairman ");
builder.InsertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.InsertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.MoveToMergeField("Chairman");
builder.Bold = true;
builder.Writeln("John Doe");

builder.MoveToMergeField("ChiefFinancialOfficer");
builder.Italic = true;
builder.Writeln("Jane Doe");

builder.MoveToMergeField("ChiefTechnologyOfficer");
builder.Italic = true;
builder.Writeln("John Bloggs");

doc.Save(ArtifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

Mostra come inserire campi modulo checkbox in MERGEFIELD come unire dati durante la stampa unione.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Usa MERGEFIELD con i tag "TableStart"/"TableEnd" per definire una regione di stampa unione
    // che appartiene a un'origine dati denominata "StudentCourse" e ha un MERGEFIELD che accetta i dati da una colonna denominata "CourseName".
    builder.StartTable();
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  TableStart:StudentCourse ");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  CourseName ");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  TableEnd:StudentCourse ");
    builder.EndTable();

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertCheckBox();

    DataTable dataTable = GetStudentCourseDataTable();

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMergeEvent.InsertCheckBox.docx");

/// <summary>
/// Quando incontra un MERGEFIELD con un nome specifico, inserisce una casella di controllo nel campo del modulo invece di unire il testo dei dati.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Chiamato quando una stampa unione unisce i dati in un MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName == "CourseName")
        {
            Assert.AreEqual("StudentCourse", args.TableName);

            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.FieldName);
            builder.InsertCheckBox(args.DocumentFieldName + mCheckBoxCount, false, 0);

            string fieldValue = args.FieldValue.ToString();

            // In questo caso, per ogni record index 'n', il valore del campo corrispondente è "Corso n".
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Fare niente.
    }

    private int mCheckBoxCount;
}

/// <summary>
/// Crea un'origine dati per la stampa unione.
/// </summary>
private static DataTable GetStudentCourseDataTable()
{
    DataTable dataTable = new DataTable("StudentCourse");
    dataTable.Columns.Add("CourseName");
    for (int i = 0; i < 10; i++)
    {
        DataRow datarow = dataTable.NewRow();
        dataTable.Rows.Add(datarow);
        datarow[0] = "Course " + i;
    }

    return dataTable;
}
```

### Guarda anche

* class [DocumentBuilder](../../documentbuilder)
* spazio dei nomi [Aspose.Words](../../documentbuilder)
* assemblea [Aspose.Words](../../../)

---

## MoveToMergeField(string, bool, bool) {#movetomergefield_1}

Sposta il campo di unione nel campo di unione specificato.

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldName | String | Il nome senza distinzione tra maiuscole e minuscole del campo della stampa unione. |
| isAfter | Boolean | Se true, sposta il cursore in modo che si trovi dopo la fine del campo. Se false, sposta il cursore in modo che sia prima dell'inizio del campo. |
| isDeleteField | Boolean | Se true, elimina il campo di unione. |

### Valore di ritorno

True se il campo di unione è stato trovato e il cursore è stato spostato; falso altrimenti.

### Esempi

Mostra come inserire i campi e spostare il cursore del generatore di documenti su di essi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Sposta il cursore sul primo MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Nota che il cursore viene posizionato subito dopo il primo MERGEFIELD e prima del secondo.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Se desideriamo modificare il codice campo o il contenuto del campo utilizzando il builder,
// il suo cursore dovrebbe trovarsi all'interno di un campo.
// Per posizionarlo all'interno di un campo, dovremmo chiamare il metodo MoveTo del generatore di documenti
// e passa il nodo iniziale o separatore del campo come argomento.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Guarda anche

* class [DocumentBuilder](../../documentbuilder)
* spazio dei nomi [Aspose.Words](../../documentbuilder)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
