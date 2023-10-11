---
title: FootnoteOptions.Position
second_title: Aspose.Words for .NET API Referansı
description: FootnoteOptions mülk. Dipnotların konumunu belirtir.
type: docs
weight: 30
url: /tr/net/aspose.words.notes/footnoteoptions/position/
---
## FootnoteOptions.Position property

Dipnotların konumunu belirtir.

```csharp
public FootnotePosition Position { get; set; }
```

### Örnekler

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

* enum [FootnotePosition](../../footnoteposition/)
* class [FootnoteOptions](../)
* ad alanı [Aspose.Words.Notes](../../footnoteoptions/)
* toplantı [Aspose.Words](../../../)


