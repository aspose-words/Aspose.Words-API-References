---
title: Class FieldTC
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldTC sınıf. TC alanını uygular.
type: docs
weight: 2330
url: /tr/net/aspose.words.fields/fieldtc/
---
## FieldTC class

TC alanını uygular.

```csharp
public sealed class FieldTC : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldTC](fieldtc/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [EntryLevel](../../aspose.words.fields/fieldtc/entrylevel/) { get; set; } | Giriş düzeyini alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [OmitPageNumber](../../aspose.words.fields/fieldtc/omitpagenumber/) { get; set; } | Bu alan için İçindekiler'deki sayfa numarasının atlanıp atlanmayacağını alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [Text](../../aspose.words.fields/fieldtc/text/) { get; set; } | Girdi metnini alır veya ayarlar. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |
| [TypeIdentifier](../../aspose.words.fields/fieldtc/typeidentifier/) { get; set; } | Bu alan için (genellikle bir harf olan) bir tür tanımlayıcısı alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Notlar

İçindekiler (şekiller tablosu dahil) girişi için metin ve sayfa numarasını tanımlar, bu bir TOC alanı tarafından kullanılır.

### Örnekler

İçindekiler alanının nasıl ekleneceğini ve hangi TC alanlarının giriş olarak sonuçlanacağını filtreler.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Tüm TC alanlarını bir içindekiler tablosunda derleyecek bir TOC alanı ekleyin.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Alanı yalnızca "A" tipi TC girişlerini ve 1 ile 3 arasında bir giriş seviyesi alacak şekilde yapılandırın.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // Bu iki giriş tabloda görünecektir.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // Bu girdi, "A" dan farklı bir türe sahip olduğu için tablodan çıkarılacaktır.
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // Bu giriş, 1-3 aralığının dışında bir giriş düzeyine sahip olduğu için tablodan çıkarılacaktır.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");

/// <summary>
/// Bir TC alanı eklemek için bir belge oluşturucu kullanın.
/// </summary>
public void InsertTocEntry(DocumentBuilder builder, string text, string typeIdentifier, string entryLevel)
{
    FieldTC fieldTc = (FieldTC)builder.InsertField(FieldType.FieldTOCEntry, true);
    fieldTc.OmitPageNumber = true;
    fieldTc.Text = text;
    fieldTc.TypeIdentifier = typeIdentifier;
    fieldTc.EntryLevel = entryLevel;
}
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


