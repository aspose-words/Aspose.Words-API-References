---
title: Footnote.FootnoteType
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: .NET için Aspose.Words
description: FootnoteType özelliğini keşfedin, belgelerinizdeki dipnotları veya son notları kolayca tanımlayarak daha net ve düzenli hale getirin.
type: docs
weight: 30
url: /tr/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

Bunun bir dipnot mu yoksa sonnot mu olduğunu belirten bir değer döndürür.

```csharp
public FootnoteType FootnoteType { get; }
```

## Örnekler

Dipnotlar ile sonnotlar arasındaki farkı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda metne numaralandırılmış referanslar eklemenin iki yolu bulunmaktadır. Bu referansların her ikisi de bir
// onları eklediğimiz yerde küçük üst simge referans işareti.
// Referans işareti, varsayılan olarak, belgedeki tüm referanslar arasında referansın dizin numarasıdır.
// Her referans aynı zamanda gövde metnindeki referans işaretiyle aynı olacak bir giriş oluşturacaktır
// ve belge oluşturucunun "InsertFootnote" metoduna geçireceğimiz referans metni.
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
