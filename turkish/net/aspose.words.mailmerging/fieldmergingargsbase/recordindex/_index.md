---
title: FieldMergingArgsBase.RecordIndex
linktitle: RecordIndex
articleTitle: RecordIndex
second_title: Aspose.Words for .NET
description: FieldMergingArgsBase RecordIndex mülk. Birleştirilecek kaydın sıfır tabanlı dizinini alır C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words.mailmerging/fieldmergingargsbase/recordindex/
---
## FieldMergingArgsBase.RecordIndex property

Birleştirilecek kaydın sıfır tabanlı dizinini alır.

```csharp
public int RecordIndex { get; }
```

## Örnekler

Adres-mektup birleştirme sırasında onay kutusu form alanlarının MERGEFIELD'lere birleştirme verileri olarak nasıl ekleneceğini gösterir.

```csharp
public void InsertCheckBox()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Adres-mektup birleştirme bölgesini tanımlamak için MERGEFIELD'leri "TableStart"/"TableEnd" etiketleriyle kullanın
    // "StudentCourse" adlı bir veri kaynağına ait olan ve "CourseName" adlı bir sütundan veri kabul eden bir MERGEFIELD'a sahip olan.
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
/// Belirli bir ada sahip bir MERGEFIELD ile karşılaşıldığında, birleştirme verileri metni yerine bir onay kutusu form alanı ekler.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Adres-mektup birleştirme verileri MERGEFIELD ile birleştirdiğinde çağrılır.
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

            // Bu durumda her kayıt indeksi 'n' için karşılık gelen alan değeri "Ders n" olur.
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Hiçbir şey yapma.
    }

    private int mCheckBoxCount;
}

/// <summary>
/// Adres-mektup birleştirme veri kaynağı oluşturur.
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

### Ayrıca bakınız

* class [FieldMergingArgsBase](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
