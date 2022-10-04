---
title: MoveToMergeField
second_title: Aspose.Words for .NET API Referansı
description: İmleci belirtilen birleştirme alanının hemen ötesinde bir konuma taşır ve birleştirme alanını kaldırır.
type: docs
weight: 530
url: /tr/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(string) {#movetomergefield}

İmleci belirtilen birleştirme alanının hemen ötesinde bir konuma taşır ve birleştirme alanını kaldırır.

```csharp
public bool MoveToMergeField(string fieldName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldName | String | Adres mektup birleştirme alanının büyük/küçük harfe duyarlı olmayan adı. |

### Geri dönüş değeri

Birleştirme alanı bulunduysa ve imleç taşındıysa doğrudur; aksi halde yanlış.

### Notlar

Bu yöntemin, imleci hareket ettirdikten sonra birleştirme alanını belgeden sildiğini unutmayın.

### Örnekler

Adres mektup birleştirme yerine belge oluşturucu ile MERGEFIELD'lerin verilerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adres mektup birleştirme sırasında bir veri kaynağındaki aynı ada sahip sütunlardan veri kabul eden bazı MERGEFIELDS ekleyin,
// ve ardından bunları manuel olarak doldurun.
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

Adres mektup birleştirme sırasında birleştirme verileri olarak MERGEFIELD'lere onay kutusu form alanlarının nasıl ekleneceğini gösterir.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Adres mektup birleştirme bölgesi tanımlamak için "TableStart"/"TableEnd" etiketleriyle MERGEFIELD'leri kullanın
    // "StudentCourse" adlı bir veri kaynağına ait olan ve "CourseName" adlı bir sütundan veri kabul eden bir MERGEFIELD'e sahip.
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
/// Belirli bir ada sahip bir MERGEFIELD ile karşılaşıldığında, birleştirme veri metni yerine bir onay kutusu form alanı ekler.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Adres mektup birleştirme verileri bir MERGEFIELD ile birleştirdiğinde çağrılır.
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

            // Bu durumda, her kayıt indeksi 'n' için karşılık gelen alan değeri "Ders n"dir.
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
/// Adres mektup birleştirme veri kaynağı oluşturur.
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

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## MoveToMergeField(string, bool, bool) {#movetomergefield_1}

Birleştirme alanını belirtilen birleştirme alanına taşır.

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldName | String | Adres mektup birleştirme alanının büyük/küçük harfe duyarlı olmayan adı. |
| isAfter | Boolean | Doğru olduğunda, imleci alan bitiminden sonra olacak şekilde hareket ettirir. Yanlış olduğunda, imleci alan başlangıcından önce olacak şekilde hareket ettirir. |
| isDeleteField | Boolean | Doğru olduğunda, birleştirme alanını siler. |

### Geri dönüş değeri

Birleştirme alanı bulunduysa ve imleç taşındıysa doğrudur; aksi halde yanlış.

### Örnekler

Alanların nasıl ekleneceğini ve belge oluşturucunun imlecinin bu alanlara nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// İmleci ilk MERGEFIELD'e taşıyın.
builder.MoveToMergeField("MyMergeField1", true, false);

// İmlecin ilk MERGEFIELD'den hemen sonra ve ikinciden önce yerleştirildiğini unutmayın.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Oluşturucuyu kullanarak alanın alan kodunu veya içeriğini düzenlemek istiyorsak,
// imlecinin bir alanın içinde olması gerekir.
// Bir alanın içine yerleştirmek için belge oluşturucunun MoveTo yöntemini çağırmamız gerekir
// ve alanın başlangıç veya ayırıcı düğümünü argüman olarak iletin.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
