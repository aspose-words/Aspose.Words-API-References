---
title: EndnotePosition Enum
linktitle: EndnotePosition
articleTitle: EndnotePosition
second_title: Aspose.Words for .NET
description: Aspose.Words.Notes.EndnotePosition Sıralama. Son not konumunu tanımlar C#'da.
type: docs
weight: 4250
url: /tr/net/aspose.words.notes/endnoteposition/
---
## EndnotePosition enumeration

Son not konumunu tanımlar.

```csharp
public enum EndnotePosition
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| EndOfSection | `0` | Son notlar bölümün sonunda çıkarılır. |
| EndOfDocument | `3` | Son notlar belgenin sonunda görüntülenir. |

## Örnekler

Belgenin son notlarını toplayıp görüntüleyeceği farklı bir yerin nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Son not, metne bir referans veya yan yorum eklemenin bir yoludur
 // bu, ana gövde metninin akışına müdahale etmez.
// Son notun eklenmesi küçük bir üst simge referans sembolü ekler
// ana gövde metninde son notu eklediğimiz yer.
// Her son not ayrıca belgenin sonunda bir sembolden oluşan bir giriş oluşturur
// ana gövde metnindeki referans sembolüyle eşleşen.
// Belge oluşturucunun "InsertEndnote" yöntemine ilettiğimiz referans metni.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Belgenin tüm son notlarını nereye yerleştireceğini belirlemek için "Konum" özelliğini kullanabiliriz.
// "Position" özelliğinin değerini "EndnotePosition.EndOfDocument" olarak ayarlarsak,
// her dipnot belgenin sonunda bir koleksiyonda görünecektir. Bu varsayılan değerdir.
// "Position" özelliğinin değerini "EndnotePosition.EndOfSection" olarak ayarlarsak,
// her dipnot, metni sonnotun referans işaretini içeren bölümün sonunda bir koleksiyonda görünecektir.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

### Ayrıca bakınız

* class [EndnoteOptions](../endnoteoptions/)
* ad alanı [Aspose.Words.Notes](../../aspose.words.notes/)
* toplantı [Aspose.Words](../../)
