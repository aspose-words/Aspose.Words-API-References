---
title: EndnoteOptions.Position
linktitle: Position
articleTitle: Position
second_title: .NET için Aspose.Words
description: EndnoteOptions Position özelliğinin, dipnotlar için ideal yerleşimi belirleyerek belgenizin düzenini nasıl geliştirdiğini keşfedin. Yazınızı bugün optimize edin!
type: docs
weight: 20
url: /tr/net/aspose.words.notes/endnoteoptions/position/
---
## EndnoteOptions.Position property

Dipnotların konumunu belirtir.

```csharp
public EndnotePosition Position { get; set; }
```

## Örnekler

Belgenin dipnotlarını toplayıp görüntüleyeceği farklı bir yerin nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Son not, metne bir referans veya yan yorum eklemenin bir yoludur
 // ana gövde metninin akışını engellemeyen.
// Bir dipnot eklemek, küçük bir üst simge referans sembolü ekler
// dipnotu eklediğimiz ana metinde.
// Her dipnot ayrıca belgenin sonunda bir sembolden oluşan bir giriş oluşturur
// ana gövde metnindeki referans sembolüyle eşleşen.
// Belge oluşturucunun "InsertEndnote" metoduna geçirdiğimiz referans metni.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// Belgenin tüm dipnotlarının nereye yerleştirileceğini belirlemek için "Konum" özelliğini kullanabiliriz.
// "Position" özelliğinin değerini "EndnotePosition.EndOfDocument" olarak ayarlarsak,
// her dipnot belgenin sonunda bir koleksiyonda gösterilecektir. Bu varsayılan değerdir.
// "Position" özelliğinin değerini "EndnotePosition.EndOfSection" olarak ayarlarsak,
// her dipnot, dipnotun referans işaretini içeren bölümün sonundaki bir koleksiyonda görünecektir.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

### Ayrıca bakınız

* enum [EndnotePosition](../../endnoteposition/)
* class [EndnoteOptions](../)
* ad alanı [Aspose.Words.Notes](../../../aspose.words.notes/)
* toplantı [Aspose.Words](../../../)
