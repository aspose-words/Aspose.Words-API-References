---
title: EndnoteOptions.Position
second_title: Aspose.Words for .NET API Referansı
description: EndnoteOptions mülk. Son notların konumunu belirtir.
type: docs
weight: 20
url: /tr/net/aspose.words.notes/endnoteoptions/position/
---
## EndnoteOptions.Position property

Son notların konumunu belirtir.

```csharp
public EndnotePosition Position { get; set; }
```

### Örnekler

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

* enum [EndnotePosition](../../endnoteposition/)
* class [EndnoteOptions](../)
* ad alanı [Aspose.Words.Notes](../../endnoteoptions/)
* toplantı [Aspose.Words](../../../)


