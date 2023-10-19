---
title: FieldNextIf.ComparisonOperator
linktitle: ComparisonOperator
articleTitle: ComparisonOperator
second_title: Aspose.Words for .NET
description: FieldNextIf ComparisonOperator mülk. Karşılaştırma operatörünü alır veya ayarlar C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldnextif/comparisonoperator/
---
## FieldNextIf.ComparisonOperator property

Karşılaştırma operatörünü alır veya ayarlar.

```csharp
public string ComparisonOperator { get; set; }
```

## Örnekler

Adres-mektup birleştirme sırasında birden çok satırı tek sayfada birleştirmek için NEXT/NEXTIF alanlarının nasıl kullanılacağını gösterir.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Adres-mektup birleştirmemiz için 3 satırlı bir veri kaynağı oluşturun.
    // Bu tabloyu kullanan bir adres-mektup birleştirme normalde 3 sayfalık bir belge oluşturur.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Aynı AlanAdına sahip birden fazla birleştirme alanımız varsa,
    // veri kaynağının aynı satırından veri alacaklar ve birleştirme sonrasında aynı değeri gösterecekler.
    // NEXT alanı adres-mektup birleştirmeye anında bir satır aşağı gitmesini söyler,
    // bu, NEXT alanını takip eden tüm MERGEFIELD'lerin bir sonraki satırdan veri alacağı anlamına gelir.
    // Zaten son satırdayken asla bir sonraki satıra atlamaya çalışmadığınızdan emin olun.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // Birleştirme sonrasında bu MERGEFIELD'lerin kabul ettiği veri kaynağı değerleri
     // yukarıdaki MERGEFIELD'lerle aynı sayfada yer alacak.
    InsertMergeFields(builder, "Second row: ");

    // NEXTIF alanı NEXT alanıyla aynı işleve sahiptir,
    // ancak yalnızca aşağıdaki 3 özellik tarafından oluşturulan bir ifade doğruysa bir sonraki satıra atlar.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // Yukarıdaki alanın ileri sürdüğü karşılaştırma doğruysa,
    // aşağıdaki 3 birleştirme alanı üçüncü satırdan veri alacaktır.
    // Aksi halde bu alanlar yine 2. satırdan veri alacaktır.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // Veri kaynağımız 3 satırdan oluşuyor ve satırları iki kere atladık.
    // Çıktı belgemiz 3 satırın tümünden gelen verileri içeren 1 sayfadan oluşacaktır.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// "Nezaket Başlığı", "Ad" ve "Soyadı" adlı sütunları içeren bir veri kaynağı için MERGEFIELD'leri eklemek üzere bir belge oluşturucu kullanır.
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// Belirtilen özelliklere sahip bir MERRGEFIELD eklemek için bir belge oluşturucu kullanır.
/// </summary>
public void InsertMergeField(DocumentBuilder builder, string fieldName, string textBefore, string textAfter)
{
    FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, true);
    field.FieldName = fieldName;
    field.TextBefore = textBefore;
    field.TextAfter = textAfter;
}
```

### Ayrıca bakınız

* class [FieldNextIf](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
