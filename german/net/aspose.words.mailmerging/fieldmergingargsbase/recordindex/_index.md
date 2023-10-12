---
title: FieldMergingArgsBase.RecordIndex
second_title: Aspose.Words für .NET-API-Referenz
description: FieldMergingArgsBase eigendom. Ruft den nullbasierten Index des Datensatzes ab der zusammengeführt wird.
type: docs
weight: 60
url: /de/net/aspose.words.mailmerging/fieldmergingargsbase/recordindex/
---
## FieldMergingArgsBase.RecordIndex property

Ruft den nullbasierten Index des Datensatzes ab, der zusammengeführt wird.

```csharp
public int RecordIndex { get; }
```

### Beispiele

Zeigt, wie Kontrollkästchen-Formularfelder als Seriendaten während des Seriendrucks in MERGEFIELDs eingefügt werden.

```csharp
public void InsertCheckBox()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Verwenden Sie MERGEFIELDs mit den Tags „TableStart“/„TableEnd“, um einen Seriendruckbereich zu definieren
    // das zu einer Datenquelle namens „StudentCourse“ gehört und über ein MERGEFIELD verfügt, das Daten aus einer Spalte namens „CourseName“ akzeptiert.
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
/// Wenn ein MERGEFIELD mit einem bestimmten Namen gefunden wird, wird anstelle des Zusammenführungsdatentextes ein Kontrollkästchen-Formularfeld eingefügt.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Wird aufgerufen, wenn ein Serienbrief Daten in einem MERGEFIELD zusammenführt.
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

            // In diesem Fall ist für jeden Datensatzindex „n“ der entsprechende Feldwert „Kurs n“.
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Nichts tun.
    }

    private int mCheckBoxCount;
}

/// <summary>
/// Erstellt eine Serienbrief-Datenquelle.
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

### Siehe auch

* class [FieldMergingArgsBase](../)
* namensraum [Aspose.Words.MailMerging](../../fieldmergingargsbase/)
* Montage [Aspose.Words](../../../)


