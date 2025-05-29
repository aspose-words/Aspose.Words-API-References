---
title: FootnotePosition Enum
linktitle: FootnotePosition
articleTitle: FootnotePosition
second_title: .NET için Aspose.Words
description: Özelleştirilebilir dipnot yerleşimi, belge biçimlendirmesinin iyileştirilmesi ve okunabilirlik için Aspose.Words.Notes.FootnotePosition numaralandırmasını keşfedin.
type: docs
weight: 4980
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
| BottomOfPage | `1` | Dipnotlar her sayfanın alt kısmında çıktı olarak verilir. |
| BeneathText | `2` | Dipnotlar her sayfadaki metnin altında çıktı olarak verilir. |

## Örnekler

Belgenin dipnotlarını toplayıp görüntüleyeceği farklı bir yerin nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dipnot, metne bir referans veya yan yorum eklemenin bir yoludur
 // ana gövde metninin akışını engellemeyen.
// Dipnot eklemek, küçük bir üst simge referans sembolü ekler
// Dipnotu eklediğimiz ana metinde.
// Her dipnot ayrıca sayfanın en altında bir giriş oluşturur ve bu giriş bir sembolden oluşur
// ana gövde metnindeki referans sembolüyle eşleşen.
// Belge oluşturucunun "InsertFootnote" metoduna geçirdiğimiz referans metni.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// Belgenin tüm dipnotlarının nereye yerleştirileceğini belirlemek için "Konum" özelliğini kullanabiliriz.
// "Position" özelliğinin değerini "FootnotePosition.BottomOfPage" olarak ayarlarsak,
// her dipnot, referans işaretini içeren sayfanın en altında görünecektir. Bu varsayılan değerdir.
// "Position" özelliğinin değerini "FootnotePosition.BeneathText" olarak ayarlarsak,
// her dipnot, referans işaretini içeren sayfanın metninin sonunda görünecektir.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### Ayrıca bakınız

* class [FootnoteOptions](../footnoteoptions/)
* ad alanı [Aspose.Words.Notes](../../aspose.words.notes/)
* toplantı [Aspose.Words](../../)
