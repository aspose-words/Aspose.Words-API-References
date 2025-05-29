---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
linktitle: IncludeTextboxesFootnotesEndnotesInStat
articleTitle: IncludeTextboxesFootnotesEndnotesInStat
second_title: .NET için Aspose.Words
description: IncludeTextboxesFootnotesEndnotesInStat özelliğiyle belgenizin kelime sayısını optimize edin. Metin kutularını, dipnotları ve son notları zahmetsizce kontrol edin!
type: docs
weight: 230
url: /tr/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

Kelime sayısı istatistiklerine metin kutuları, dipnotlar ve son notların dahil edilip edilmeyeceğini belirtir.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

## Örnekler

Kelime sayısı istatistiklerine metin kutularının, dipnotların ve son notların nasıl dahil edileceğini veya hariç tutulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// Varsayılan olarak seçenek 'false' olarak ayarlanmıştır.
doc.UpdateWordCount();
// Kelimeler metin kutuları, dipnotlar ve sonnotlar olmadan sayılır.
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// Metin kutuları, dipnotlar ve sonnotlarda kelime sayısı.
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
