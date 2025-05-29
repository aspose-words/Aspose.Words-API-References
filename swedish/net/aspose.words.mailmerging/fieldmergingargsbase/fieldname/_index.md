---
title: FieldMergingArgsBase.FieldName
linktitle: FieldName
articleTitle: FieldName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldName i FieldMergingArgsBase, som hämtar namnet på kopplingsfältet från din datakälla för sömlös integration.
type: docs
weight: 40
url: /sv/net/aspose.words.mailmerging/fieldmergingargsbase/fieldname/
---
## FieldMergingArgsBase.FieldName property

Hämtar namnet på kopplingsfältet i datakällan.

```csharp
public string FieldName { get; }
```

## Anmärkningar

Om du har en mappning från ett dokumentfältnamn till ett annat datakällfältnamn, , så är detta det mappade fältnamnet.

Om du angav ett fältnamnsprefix, till exempel "Bild:MittFältnamn" i dokumentet, så`FieldName` returnerar fältnamnet utan prefixet, det vill säga "MittFältnamn".

## Exempel

Visar hur man infogar kryssrutefält i MERGEFIELDS som kopplingsdata under dokumentkoppling.

```csharp
public void InsertCheckBox()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Använd MERGEFIELDs med taggarna "TableStart"/"TableEnd" för att definiera ett område för dokumentkoppling
    // som tillhör en datakälla med namnet "StudentCourse" och har ett MERGEFIELD som accepterar data från en kolumn med namnet "CourseName".
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
/// När ett MERGEFIELD med ett specifikt namn påträffas, infogas ett kryssruteformulärfält istället för text för sammanfogningsdata.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Anropas när en dokumentkoppling sammanfogar data till ett MERGEFIELD.
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

            // I det här fallet är motsvarande fältvärde "Kurs n" för varje postindex 'n'.
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Gör ingenting.
    }

    private int mCheckBoxCount;
}

/// <summary>
/// Skapar en datakälla för dokumentkoppling.
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
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
