---
title: FootnotePosition Enum
linktitle: FootnotePosition
articleTitle: FootnotePosition
second_title: Aspose.Words for .NET
description: Aspose.Words.Notes.FootnotePosition Sıralama. Dipnot konumunu tanımlar C#'da.
type: docs
weight: 4290
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
| BottomOfPage | `1` | Dipnotlar her sayfanın altında görüntülenir. |
| BeneathText | `2` | Dipnotlar her sayfadaki metnin altında görüntülenir. |

## Örnekler

Belgenin dipnotlarını toplayıp görüntüleyeceği farklı bir yerin nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dipnot, metne referans veya yan yorum eklemenin bir yoludur
 // bu, ana gövde metninin akışına müdahale etmez.
// Dipnot eklemek küçük bir üst simge referans sembolü ekler
// ana gövde metninde dipnotu eklediğimiz yere.
// Her dipnot ayrıca sayfanın altında bir sembolden oluşan bir giriş oluşturur
// ana gövde metnindeki referans sembolüyle eşleşen.
// Belge oluşturucunun "InsertFootnote" yöntemine ilettiğimiz referans metni.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Belgenin tüm dipnotlarını nereye yerleştireceğini belirlemek için "Konum" özelliğini kullanabiliriz.
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
