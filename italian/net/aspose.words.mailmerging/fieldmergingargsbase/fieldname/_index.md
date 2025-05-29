---
title: FieldMergingArgsBase.FieldName
linktitle: FieldName
articleTitle: FieldName
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldName di FieldMergingArgsBase, che recupera il nome del campo di unione dalla tua origine dati per un'integrazione perfetta.
type: docs
weight: 40
url: /it/net/aspose.words.mailmerging/fieldmergingargsbase/fieldname/
---
## FieldMergingArgsBase.FieldName property

Ottiene il nome del campo di unione nell'origine dati.

```csharp
public string FieldName { get; }
```

## Osservazioni

Se si dispone di una mappatura dal nome di un campo di un documento a un nome di campo di un'origine dati diversa, , questo è il nome del campo mappato.

Se hai specificato un prefisso del nome del campo, ad esempio "Immagine:NomeCampo" nel documento, allora`FieldName` restituisce il nome del campo senza prefisso, ovvero "MyFieldName".

## Esempi

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

* class [FieldMergingArgsBase](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
