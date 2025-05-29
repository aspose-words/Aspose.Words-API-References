---
title: FieldAutoNumOut Class
linktitle: FieldAutoNumOut
articleTitle: FieldAutoNumOut
second_title: .NET için Aspose.Words
description: Sorunsuz AUTONUMOUT alan uygulaması için Aspose.Words.Fields.FieldAutoNumOut sınıfını keşfedin, belge otomasyonunu ve verimliliğini artırın.
type: docs
weight: 2010
url: /tr/net/aspose.words.fields/fieldautonumout/
---
## FieldAutoNumOut class

AUTONUMOUT alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldAutoNumOut : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldAutoNumOut](fieldautonumout/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
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

Anahat biçiminde otomatik bir sayı ekler.

## Örnekler

AUTONUMOUT alanlarını kullanarak paragrafların nasıl numaralandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// AUTONUMOUT alanları her AUTONUMOUT alanında artan bir sayı görüntüler.
// AUTONUM alanlarının aksine, AUTONUMOUT alanları anahat numaralandırma şemasını kullanır,
// Microsoft Word'de Biçim -> Madde İşaretleri ve Numaralandırma -> "Anahat Numaralandırılmış" yoluyla tanımlayabileceğimiz.
// Bu, numaralı bir liste gibi öğeleri otomatik olarak numaralandırmamızı sağlar.
// LISTNUM alanları AUTONUMOUT alanlarına göre daha yeni bir alternatiftir.
// Bu alanda "1." gösterilecektir.
builder.InsertField(FieldType.FieldAutoNumOutline, true);
builder.Writeln("\tParagraph 1.");

// Bu alanda "2." gösterilecektir.
builder.InsertField(FieldType.FieldAutoNumOutline, true);
builder.Writeln("\tParagraph 2.");

foreach (FieldAutoNumOut field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumOutline).ToList())
    Assert.AreEqual(" AUTONUMOUT ", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUMOUT.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
