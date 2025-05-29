---
title: FieldMergingArgsBase.TableName
linktitle: TableName
articleTitle: TableName
second_title: .NET için Aspose.Words
description: FieldMergingArgsBase TableName özelliğini keşfedin, birleştirme işlemleriniz için veri tablosu adına kolayca erişin veya kullanılamadığında bunu bilin.
type: docs
weight: 70
url: /tr/net/aspose.words.mailmerging/fieldmergingargsbase/tablename/
---
## FieldMergingArgsBase.TableName property

Geçerli birleştirme işlemi için veri tablosunun adını veya ad mevcut değilse boş dizeyi alır.

```csharp
public string TableName { get; }
```

## Örnekler

Posta birleştirme sırasında MERGEFIELD'lara birleştirme verisi olarak onay kutusu form alanlarının nasıl ekleneceğini gösterir.

```csharp
public void InsertCheckBox()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bir posta birleştirme bölgesini tanımlamak için "TableStart"/"TableEnd" etiketleriyle MERGEFIELD'leri kullanın
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
/// Belirli bir ada sahip bir MERGEFIELD ile karşılaşıldığında, birleştirme veri metni yerine bir onay kutusu form alanı ekler.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Bir posta birleştirme işlemi verileri bir MERGEFIELD'a birleştirdiğinde çağrılır.
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

            // Bu durumda her kayıt indeksi 'n' için karşılık gelen alan değeri "Course n"dir.
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Hiçbir şey yapmayın.
    }

    private int mCheckBoxCount;
}

/// <summary>
/// Bir posta birleştirme veri kaynağı oluşturur.
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
