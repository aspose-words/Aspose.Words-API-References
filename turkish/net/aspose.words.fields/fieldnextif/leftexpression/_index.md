---
title: FieldNextIf.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: .NET için Aspose.Words
description: FieldNextIf LeftExpression özelliğini keşfedin. Gelişmiş veri işleme ve analizi için karşılaştırma ifadelerinizin sol tarafını kolayca yönetin.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldnextif/leftexpression/
---
## FieldNextIf.LeftExpression property

Karşılaştırma ifadesinin sol kısmını alır veya ayarlar.

```csharp
public string LeftExpression { get; set; }
```

## Örnekler

Bir posta birleştirme sırasında birden fazla satırı tek bir sayfada birleştirmek için NEXT/NEXTIF alanlarının nasıl kullanılacağını gösterir.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // E-posta birleştirmemiz için 3 satırdan oluşan bir veri kaynağı oluşturalım.
    // Bu tabloyu kullanan bir posta birleştirme işlemi normalde 3 sayfalık bir belge oluşturur.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Aynı FieldName'e sahip birden fazla birleştirme alanımız varsa,
    // veri kaynağının aynı satırından veri alacaklar ve birleştirmeden sonra aynı değeri görüntüleyecekler.
    // SONRAKİ alanı, posta birleştirmeye anında bir satır aşağı hareket etmesini söyler,
    // bu, NEXT alanını takip eden tüm MERGEFIELD'ların bir sonraki satırdan veri alacağı anlamına gelir.
    // Son satırdayken bir sonraki satıra geçmeye kesinlikle çalışmayın.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // Birleştirmeden sonra, bu MERGEFIELD'lerin kabul ettiği veri kaynağı değerleri
     // yukarıdaki MERGEFIELD'larla aynı sayfada sonlanacaktır.
    InsertMergeFields(builder, "Second row: ");

    // NEXTIF alanı, NEXT alanıyla aynı işleve sahiptir.
    // ancak aşağıdaki 3 özellik tarafından oluşturulan bir ifade doğruysa bir sonraki satıra atlar.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // Yukarıdaki alan tarafından iddia edilen karşılaştırma doğruysa,
    // Aşağıdaki 3 birleştirme alanı üçüncü satırdan veri alacaktır.
    // Aksi halde bu alanlar tekrar 2. satırdan veri alacaktır.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // Veri kaynağımızda 3 satır var ve iki kez satır atladık.
    // Çıktı belgemiz, 3 satırın tümünden veri içeren 1 sayfadan oluşacaktır.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// "Nezaket Ünvanı", "Adı" ve "Soyadı" adlı sütunları içeren bir veri kaynağı için MERGEFIELD'leri eklemek üzere bir belge oluşturucu kullanır.
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// Belirtilen özelliklere sahip bir MERGFEILD eklemek için bir belge oluşturucu kullanır.
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
