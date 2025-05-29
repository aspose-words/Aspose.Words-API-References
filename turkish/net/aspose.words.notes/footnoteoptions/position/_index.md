---
title: FootnoteOptions.Position
linktitle: Position
articleTitle: Position
second_title: .NET için Aspose.Words
description: FootnoteOptions Position özelliğinin, dipnot yerleşimini hassas bir şekilde kontrol ederek okunabilirliği artırarak belge düzeninizi nasıl iyileştirdiğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.notes/footnoteoptions/position/
---
## FootnoteOptions.Position property

Dipnotların konumunu belirtir.

```csharp
public FootnotePosition Position { get; set; }
```

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

* enum [FootnotePosition](../../footnoteposition/)
* class [FootnoteOptions](../)
* ad alanı [Aspose.Words.Notes](../../../aspose.words.notes/)
* toplantı [Aspose.Words](../../../)
