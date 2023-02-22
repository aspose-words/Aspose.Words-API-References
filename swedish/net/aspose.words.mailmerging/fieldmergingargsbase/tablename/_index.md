---
title: FieldMergingArgsBase.TableName
second_title: Aspose.Words för .NET API Referens
description: FieldMergingArgsBase fast egendom. Hämtar namnet på datatabellen för den aktuella sammanslagningsoperationen eller tom sträng om namnet inte är tillgängligt.
type: docs
weight: 70
url: /sv/net/aspose.words.mailmerging/fieldmergingargsbase/tablename/
---
## FieldMergingArgsBase.TableName property

Hämtar namnet på datatabellen för den aktuella sammanslagningsoperationen eller tom sträng om namnet inte är tillgängligt.

```csharp
public string TableName { get; }
```

### Exempel

Visar hur man infogar kryssrutaformulär i MERGEFIELDs som sammanfogningsdata under sammanfogning.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Använd MERGEFIELDs med "TableStart"/"TableEnd"-taggar för att definiera en kopplingsregion
    // som tillhör en datakälla som heter "StudentCourse" och har ett MERGEFIELD som accepterar data från en kolumn som heter "CourseName".
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
/// När du stöter på ett MERGEFIELD med ett specifikt namn, infogar ett kryssrutaformulärfält istället för sammanslagningsdatatext.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Anropas när en e-postsammanfogning slår samman data till ett MERGEFIELD.
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

            // I detta fall, för varje postindex 'n', är motsvarande fältvärde "Course n".
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Göra ingenting.
    }

    private int mCheckBoxCount;
}

/// <summary>
/// Skapar en kopplingsdatakälla.
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

### Se även

* class [FieldMergingArgsBase](../)
* namnutrymme [Aspose.Words.MailMerging](../../fieldmergingargsbase/)
* hopsättning [Aspose.Words](../../../)


