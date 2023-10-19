---
title: FieldNext Class
linktitle: FieldNext
articleTitle: FieldNext
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldNext sınıf. SONRAKİ alanını uygular C#'da.
type: docs
weight: 2180
url: /tr/net/aspose.words.fields/fieldnext/
---
## FieldNext class

SONRAKİ alanını uygular.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

```csharp
public class FieldNext : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldNext](fieldnext/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir alır[`FieldFormat`](../fieldformat/) Alanın formatlamasına yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplanmamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. Olabilir`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son child 'si ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa şunu döndürür:`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alanın bağlantısını kaldırır. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

## Notlar

Yeni bir birleştirilmiş belge a başlatmak yerine, sonraki veri kaydını mevcut birleştirilmiş belgeyle birleştirir.

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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
