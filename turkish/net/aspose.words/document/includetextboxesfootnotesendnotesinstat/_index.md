---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words for .NET API Referansı
description: Document mülk. Kelime sayısı istatistiklerine metin kutularının dipnotların ve son notların dahil edilip edilmeyeceğini belirtir.
type: docs
weight: 220
url: /tr/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

Kelime sayısı istatistiklerine metin kutularının, dipnotların ve son notların dahil edilip edilmeyeceğini belirtir.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

### Örnekler

Metin kutularının, dipnotların ve son notların kelime sayısı istatistiklerine nasıl dahil edileceğini veya hariç tutulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// Varsayılan olarak seçenek 'yanlış' olarak ayarlanmıştır.
doc.UpdateWordCount();
// Kelimeler metin kutuları, dipnotlar ve son notlar olmadan sayılır.
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);            

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// Kelimeler metin kutuları, dipnotlar ve sonnotlarla sayılır.
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


