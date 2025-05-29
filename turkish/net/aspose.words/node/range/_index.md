---
title: Node.Range
linktitle: Range
articleTitle: Range
second_title: .NET için Aspose.Words
description: Düğüm Aralığı özelliğini keşfedin, gelişmiş içerik yönetimi için düğümünüz içindeki belge segmentini tanımlayan bir Aralık nesnesine zahmetsizce erişin.
type: docs
weight: 80
url: /tr/net/aspose.words/node/range/
---
## Node.Range property

Bir[`Range`](../../range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne.

```csharp
public Range Range { get; }
```

## Örnekler

Bir aralıktaki tüm düğümlerin nasıl silineceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgedeki ilk bölüme metin ekleyin ve ardından başka bir bölüm ekleyin.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// Tüm düğümleri kaldırarak ilk bölümü tamamen kaldırın
// bölümün kendisi de dahil olmak üzere kendi aralığı içinde.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Range](../../range/)
* class [Node](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
