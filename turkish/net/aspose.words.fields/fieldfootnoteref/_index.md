---
title: Class FieldFootnoteRef
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldFootnoteRef sınıf. FOOTNOTEREF alanını uygular.
type: docs
weight: 1750
url: /tr/net/aspose.words.fields/fieldfootnoteref/
---
## FieldFootnoteRef class

FOOTNOTEREF alanını uygular.

```csharp
public class FieldFootnoteRef : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldFootnoteRef](fieldfootnoteref/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Örnekler

FOOTNOTEREF alanıyla dipnotlara nasıl çapraz referans verileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("CrossRefBookmark");
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Cross referenced footnote.");
builder.EndBookmark("CrossRefBookmark");
builder.InsertParagraph();

// Aynı dipnot işaretçisini yeniden kullanırken bir dipnota birden fazla referans vermemizi sağlayan bir FOOTNOTEREF alanı ekleyin.
builder.Write("CrossReference: ");
FieldFootnoteRef field = (FieldFootnoteRef) builder.InsertField(FieldType.FieldFootnoteRef, true);

// FOOTNOTEREF alanı ile oluşturduğumuz yer imine referans verin. Bu yer imi bir dipnot işaretçisi içeriyor
// eklediğimiz dipnota ait. Alan, bu dipnot işaretçisini gösterecektir.
builder.MoveTo(field.Separator);
builder.Write("CrossRefBookmark");

Assert.AreEqual(" FOOTNOTEREF CrossRefBookmark", field.GetFieldCode());

doc.UpdateFields();

// Bu alan yalnızca Microsoft Word'ün eski sürümlerinde çalışır.
doc.Save(ArtifactsDir + "Field.FOOTNOTEREF.doc");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


