---
title: Footnote.FootnoteType
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words for .NET
description: Footnote FootnoteType mülk. Bunun dipnot mu yoksa son not mu olduğunu belirten bir değer döndürür C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

Bunun dipnot mu yoksa son not mu olduğunu belirten bir değer döndürür.

```csharp
public FootnoteType FootnoteType { get; }
```

## Örnekler

Dipnotlarla sonnotlar arasındaki farkı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda metne numaralandırılmış referanslar eklemenin iki yolu verilmiştir. Bu referansların her ikisi de bir ekleyecektir
// eklediğimiz yerdeki küçük üst simge referans işareti.
// Referans işareti, varsayılan olarak, belgedeki tüm referanslar arasındaki referansın indeks numarasıdır.
// Her referans aynı zamanda gövde metnindekiyle aynı referans işaretine sahip olacak bir giriş yaratacaktır.
// ve belge oluşturucunun "InsertFootnote" yöntemine ileteceğimiz referans metni.
// 1 - Girişi, atıfta bulunduğu metinle aynı sayfada görünecek bir dipnot:
builder.Write("Footnote referenced main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, 
    "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 - Girişi belgenin sonunda görünecek bir son not:
builder.Write("Endnote referenced main body text.");
Footnote endnote = builder.InsertFootnote(FootnoteType.Endnote, 
    "Endnote text, will appear at the very end of the document.");

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(FootnoteType.Footnote, footnote.FootnoteType);
Assert.AreEqual(FootnoteType.Endnote, endnote.FootnoteType);

doc.Save(ArtifactsDir + "InlineStory.FootnoteEndnote.docx");
```

### Ayrıca bakınız

* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* ad alanı [Aspose.Words.Notes](../../../aspose.words.notes/)
* toplantı [Aspose.Words](../../../)
