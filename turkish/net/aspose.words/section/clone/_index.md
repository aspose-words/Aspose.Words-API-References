---
title: Section.Clone
linktitle: Clone
articleTitle: Clone
second_title: .NET için Aspose.Words
description: Section Clone yöntemimizle bölümleri zahmetsizce kopyalayın. Bu güçlü araçla iş akışınızı kolaylaştırın ve üretkenliğinizi artırın!
type: docs
weight: 130
url: /tr/net/aspose.words/section/clone/
---
## Section.Clone method

Bu bölümün bir kopyasını oluşturur.

```csharp
public Section Clone()
```

## Örnekler

Bir belgeye bölümlerin nasıl ekleneceğini ve kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Belgeden ilk bölümü sil.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Şimdi ilk bölümün bir kopyasını belgenin sonuna ekleyin.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Section](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
