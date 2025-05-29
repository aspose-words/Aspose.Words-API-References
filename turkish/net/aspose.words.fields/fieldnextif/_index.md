---
title: FieldNextIf Class
linktitle: FieldNextIf
articleTitle: FieldNextIf
second_title: .NET için Aspose.Words
description: Aspose.Words.Fields.FieldNextIf sınıfını keşfedin; belge otomasyonunu geliştirmek ve iş akışlarınızı kolaylaştırmak için NEXTIF alanlarını verimli bir şekilde uygulayın.
type: docs
weight: 2600
url: /tr/net/aspose.words.fields/fieldnextif/
---
## FieldNextIf class

NEXTIF alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldNextIf : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldNextIf](fieldnextif/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldnextif/comparisonoperator/) { get; set; } | Karşılaştırma operatörünü alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LeftExpression](../../aspose.words.fields/fieldnextif/leftexpression/) { get; set; } | Karşılaştırma ifadesinin sol kısmını alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [RightExpression](../../aspose.words.fields/fieldnextif/rightexpression/) { get; set; } | Karşılaştırma ifadesinin doğru kısmını alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son alt 'siyse, üst paragrafını döndürür. Alan zaten kaldırılmışsa, şunu döndürür`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alan bağlantısını kaldırma işlemini gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |

## Notlar

İfadelerle belirtilen değerleri karşılaştırır[`LeftExpression`](./leftexpression/) Ve[`RightExpression`](./rightexpression/) ile belirtilen operatör kullanılarak karşılaştırma[`ComparisonOperator`](./comparisonoperator/) . Karşılaştırma doğruysa, sonraki veri kaydı geçerli birleştirme belgesine birleştirilir. (main belgesindeki NEXTIF'i izleyen birleştirme alanları, geçerli veri kaydı yerine sonraki veri kaydındaki değerlerle değiştirilir.) Karşılaştırma yanlışsa, sonraki veri kaydı yeni bir birleştirme belgesine birleştirilir.

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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
