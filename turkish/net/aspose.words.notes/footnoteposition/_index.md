---
title: Enum FootnotePosition
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Notes.FootnotePosition Sıralama. Dipnot konumunu tanımlar.
type: docs
weight: 4050
url: /tr/net/aspose.words.notes/footnoteposition/
---
## FootnotePosition enumeration

Dipnot konumunu tanımlar.

```csharp
public enum FootnotePosition
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| BottomOfPage | `1` | Dipnotlar her sayfanın alt kısmında gösterilir. |
| BeneathText | `2` | Dipnotlar, her sayfadaki metnin altında görüntülenir. |

### Örnekler

Belgenin dipnotlarını topladığı ve görüntülediği farklı bir yerin nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dipnot, metne referans veya yan yorum eklemenin bir yoludur
// ana gövde metninin akışını engellemez.  
// Bir dipnot eklemek, küçük bir üst simge referans sembolü ekler
// dipnotu eklediğimiz ana gövde metninde.
// Her dipnot ayrıca sayfanın altında bir sembolden oluşan bir giriş oluşturur.
// ana gövde metnindeki referans sembolüyle eşleşen.
// Belge oluşturucunun "InsertFootnote" yöntemine aktardığımız referans metni.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Belgenin tüm dipnotlarını nereye yerleştireceğini belirlemek için "Pozisyon" özelliğini kullanabiliriz.
// "Position" özelliğinin değerini "FootnotePosition.BottomOfPage" olarak ayarlarsak,
// her dipnot, referans işaretini içeren sayfanın altında görünecektir. Bu varsayılan değerdir.
// "Position" özelliğinin değerini "FootnotePosition.BeneathText" olarak ayarlarsak,
// her dipnot, referans işaretini içeren sayfa metninin sonunda görünecektir.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### Ayrıca bakınız

* class [FootnoteOptions](../footnoteoptions/)
* ad alanı [Aspose.Words.Notes](../../aspose.words.notes/)
* toplantı [Aspose.Words](../../)


