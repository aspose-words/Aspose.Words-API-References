---
title: Paragraph.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: .NET için Aspose.Words
description: Word'deki Paragraph IsInsertRevision özelliğini keşfedin. Verimli belge yönetimi için değişiklik izleme sırasında eklenen metni nasıl tanımladığını öğrenin.
type: docs
weight: 110
url: /tr/net/aspose.words/paragraph/isinsertrevision/
---
## Paragraph.IsInsertRevision property

Bu nesnenin Microsoft Word'e değişiklik izleme etkinleştirilmişken eklenip eklenmediğini döndürür.

```csharp
public bool IsInsertRevision { get; }
```

## Örnekler

Gözden geçirme paragraflarıyla nasıl çalışılacağını gösterir.

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

// Bu tür paragraflar, silme revizyonunu kabul veya reddedene kadar kalacaktır.
// Revizyonu kabul etmek paragrafı tamamen kaldıracaktır,
// ve revizyonu reddetmek, onu hiç silmemişiz gibi belgede bırakacaktır.
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// Revizyonu kabul edin ve ardından paragrafın gittiğini doğrulayın.
doc.AcceptAllRevisions();

Assert.AreEqual(3, paragraphs.Count);
Assert.AreEqual(0, para.Count);
Assert.AreEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
