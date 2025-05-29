---
title: DocumentBuilder.MoveToMergeField
linktitle: MoveToMergeField
articleTitle: MoveToMergeField
second_title: .NET için Aspose.Words
description: MoveToMergeField yöntemiyle belgenizde zahmetsizce gezinin. Sorunsuz düzenleme için imleci anında birleştirme alanlarının ötesine konumlandırın.
type: docs
weight: 590
url: /tr/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(*string*) {#movetomergefield}

İmleci belirtilen birleştirme alanının hemen ötesine taşır ve birleştirme alanını kaldırır.

```csharp
public bool MoveToMergeField(string fieldName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldName | String | Posta birleştirme alanının büyük/küçük harfe duyarlı olmayan adı. |

### Geri dönüş değeri

`doğru` birleştirme alanı bulunduysa ve imleç hareket ettirildiyse;`YANLIŞ` aksi takdirde.

## Notlar

Bu yöntemin, imleci hareket ettirdikten sonra birleştirme alanını belgeden sildiğini unutmayın.

## Örnekler

Bir posta birleştirme yerine bir belge oluşturucu kullanarak MERGEFIELD'ların verilerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir posta birleştirme sırasında bir veri kaynağındaki aynı adlı sütunlardan veri kabul eden bazı MERGEFIELDS'leri ekleyin,
// ve sonra bunları elle doldurun.
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

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## MoveToMergeField(*string, bool, bool*) {#movetomergefield_1}

Birleştirme alanını belirtilen birleştirme alanına taşır.

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldName | String | Posta birleştirme alanının büyük/küçük harfe duyarlı olmayan adı. |
| isAfter | Boolean | Ne zaman`doğru` , imleci alan sonundan sonraya taşır. `YANLIŞ` , imleci alan başlangıcından önceye taşır. |
| isDeleteField | Boolean | Ne zaman`doğru`, birleştirme alanını siler. |

### Geri dönüş değeri

`doğru` birleştirme alanı bulunduysa ve imleç hareket ettirildiyse;`YANLIŞ` aksi takdirde.

## Örnekler

Alanların nasıl ekleneceğini ve belge oluşturucunun imlecinin bunlara nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// İmleci ilk MERGEFIELD'a taşı.
builder.MoveToMergeField("MyMergeField1", true, false);

// İmlecin ilk MERGEFIELD'dan hemen sonra, ikinciden ise önce yerleştirildiğine dikkat edin.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Alanın alan kodunu veya içeriğini oluşturucuyu kullanarak düzenlemek istersek,
// imlecinin bir alanın içerisinde olması gerekir.
// Bunu bir alanın içine yerleştirmek için, belge oluşturucunun MoveTo yöntemini çağırmamız gerekir
// ve alanın başlangıç veya ayırıcı düğümünü argüman olarak geçirin.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
