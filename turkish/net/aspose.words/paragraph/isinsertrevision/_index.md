---
title: Paragraph.IsInsertRevision
second_title: Aspose.Words for .NET API Referansı
description: Paragraph mülk. Bu nesne Microsoft Worde değişiklik izleme etkinken eklenmişse doğru değerini döndürür.
type: docs
weight: 110
url: /tr/net/aspose.words/paragraph/isinsertrevision/
---
## Paragraph.IsInsertRevision property

Bu nesne Microsoft Word'e değişiklik izleme etkinken eklenmişse doğru değerini döndürür.

```csharp
public bool IsInsertRevision { get; }
```

### Örnekler

Revizyon paragraflarıyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2. ");
body.AppendParagraph("Paragraph 3. ");

// Yukarıdaki paragraflar revizyon değildir.
// Revizyon takibini başlattıktan sonra eklediğimiz paragraflar "Ekle" revizyonları olarak kaydedilecektir.
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// Revizyon takibini başlattıktan sonra kaldırdığımız paragraflar "Sil" revizyonları olarak kaydedilecektir.
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

// Bu tür paragraflar, silme revizyonunu kabul edene veya reddedene kadar kalacaktır.
// Düzeltmeyi kabul etmek paragrafı tamamen kaldıracaktır,
// ve revizyonu reddetmek, onu sanki hiç silmemişiz gibi belgede bırakacaktır.
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// Düzeltmeyi kabul edin ve ardından paragrafın kaybolduğunu doğrulayın.
doc.AcceptAllRevisions();

Assert.AreEqual(3, paragraphs.Count);
Assert.That(para, Is.Empty);
Assert.AreEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../paragraph/)
* toplantı [Aspose.Words](../../../)


