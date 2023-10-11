---
title: FieldMergingArgsBase.FieldName
second_title: Aspose.Words for .NET API Referansı
description: FieldMergingArgsBase mülk. Veri kaynağındaki birleştirme alanının adını alır.
type: docs
weight: 40
url: /tr/net/aspose.words.mailmerging/fieldmergingargsbase/fieldname/
---
## FieldMergingArgsBase.FieldName property

Veri kaynağındaki birleştirme alanının adını alır.

```csharp
public string FieldName { get; }
```

### Notlar

Bir belge alanı adından farklı bir veri kaynağı alan adına ( ) eşlemeniz varsa bu, eşlenen alan adıdır.

Belgede "Resim:AlanAdım" gibi bir alan adı öneki belirttiyseniz, ardından`FieldName` "AlanAdım" öneki olmadan alan adını döndürür.

### Örnekler

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
* ad alanı [Aspose.Words.MailMerging](../../fieldmergingargsbase/)
* toplantı [Aspose.Words](../../../)


