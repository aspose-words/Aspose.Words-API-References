---
title: DocumentBuilder.MoveToMergeField
linktitle: MoveToMergeField
articleTitle: MoveToMergeField
second_title: Aspose.Words per .NET
description: Naviga senza sforzo nel tuo documento con il metodo MoveToMergeField. Posiziona istantaneamente il cursore oltre i campi unione per una modifica fluida.
type: docs
weight: 590
url: /it/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(*string*) {#movetomergefield}

Sposta il cursore in una posizione appena oltre il campo di unione specificato e rimuove il campo di unione.

```csharp
public bool MoveToMergeField(string fieldName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldName | String | Nome del campo di stampa unione senza distinzione tra maiuscole e minuscole. |

### Valore di ritorno

`VERO` se il campo di unione è stato trovato e il cursore è stato spostato;`falso` Altrimenti.

## Osservazioni

Si noti che questo metodo elimina il campo unione dal documento dopo aver spostato il cursore.

## Esempi

Mostra come riempire i MERGEFIELD con dati tramite un generatore di documenti anziché tramite una stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire alcuni MERGEFIELDS, che accettano dati da colonne con lo stesso nome in un'origine dati durante una stampa unione,
// e poi riempirli manualmente.
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

Mostra come inserire campi modulo casella di controllo in MERGEFIELD come dati di unione durante la stampa unione.

```csharp
public void InsertCheckBox()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Utilizzare i MERGEFIELD con i tag "TableStart"/"TableEnd" per definire un'area di unione di stampa
    // che appartiene a una sorgente dati denominata "StudentCourse" e ha un MERGEFIELD che accetta dati da una colonna denominata "CourseName".
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
}

/// <summary>
/// Quando incontra un MERGEFIELD con un nome specifico, inserisce un campo modulo con casella di controllo anziché il testo dei dati di unione.
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

            // In questo caso, per ogni indice di record 'n', il valore del campo corrispondente è "Corso n".
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Non fare nulla.
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

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## MoveToMergeField(*string, bool, bool*) {#movetomergefield_1}

Sposta il campo di unione nel campo di unione specificato.

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldName | String | Nome del campo di stampa unione senza distinzione tra maiuscole e minuscole. |
| isAfter | Boolean | Quando`VERO` , sposta il cursore dopo la fine del campo. Quando`falso` , sposta il cursore prima dell'inizio del campo. |
| isDeleteField | Boolean | Quando`VERO`, elimina il campo di unione. |

### Valore di ritorno

`VERO` se il campo di unione è stato trovato e il cursore è stato spostato;`falso` Altrimenti.

## Esempi

Mostra come inserire campi e spostare su di essi il cursore del generatore di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Sposta il cursore sul primo MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Notare che il cursore viene posizionato immediatamente dopo il primo MERGEFIELD e prima del secondo.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Se desideriamo modificare il codice del campo o il contenuto utilizzando il builder,
// il cursore dovrebbe trovarsi all'interno di un campo.
// Per inserirlo all'interno di un campo, dovremmo chiamare il metodo MoveTo del generatore di documenti
// e passare il nodo iniziale o separatore del campo come argomento.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Guarda anche

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
