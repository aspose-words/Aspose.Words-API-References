---
title: FieldInclude Class
linktitle: FieldInclude
articleTitle: FieldInclude
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldInclude sınıf. INCLUDE alanını uygular C#'da.
type: docs
weight: 2030
url: /tr/net/aspose.words.fields/fieldinclude/
---
## FieldInclude class

INCLUDE alanını uygular.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

```csharp
public class FieldInclude : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldInclude](fieldinclude/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldinclude/bookmarkname/) { get; set; } | Belgeye eklenecek yer işaretinin adını alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir alır[`FieldFormat`](../fieldformat/) Alanın formatlamasına yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplanmamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [LockFields](../../aspose.words.fields/fieldinclude/lockfields/) { get; set; } | Dahil edilen belgedeki alanların güncellenmesinin engellenip engellenmeyeceğini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. Olabilir`hükümsüz` . |
| [SourceFullName](../../aspose.words.fields/fieldinclude/sourcefullname/) { get; set; } | Belgenin konumunu alır veya ayarlar. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [TextConverter](../../aspose.words.fields/fieldinclude/textconverter/) { get; set; } | Dahil edilen dosyanın biçimi için metin dönüştürücünün adını alır veya ayarlar. |
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

Başka bir belgede bulunan metin ve grafiklerin tamamını veya bir kısmını ekler.

## Örnekler

INCLUDE alanının nasıl oluşturulacağını ve özelliklerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yerel dosya sistemine başka bir belgenin bir bölümünü içe aktarmak için INCLUDE alanını kullanabiliriz.
// Bu alanla referans verdiğimiz diğer belgedeki yer imi bu içe aktarılan kısmı içeriyor.
FieldInclude field = (FieldInclude)builder.InsertField(FieldType.FieldInclude, true);
field.SourceFullName = MyDir + "Bookmarks.docx";
field.BookmarkName = "MyBookmark1";
field.LockFields = false;
field.TextConverter = "Microsoft Word";

Assert.True(Regex.Match(field.GetFieldCode(), " INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INCLUDE.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
