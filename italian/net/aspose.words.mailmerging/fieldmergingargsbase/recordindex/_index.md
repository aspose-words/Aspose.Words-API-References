---
title: FieldMergingArgsBase.RecordIndex
second_title: Aspose.Words per .NET API Reference
description: FieldMergingArgsBase proprietà. Ottiene lindice in base zero del record che viene unito.
type: docs
weight: 60
url: /it/net/aspose.words.mailmerging/fieldmergingargsbase/recordindex/
---
## FieldMergingArgsBase.RecordIndex property

Ottiene l'indice in base zero del record che viene unito.

```csharp
public int RecordIndex { get; }
```

### Esempi

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

* class [FieldMergingArgsBase](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../fieldmergingargsbase/)
* assemblea [Aspose.Words](../../../)


