---
title: Section.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words for .NET
description: Section Clone yöntem. Bu bölümün bir kopyasını oluşturur C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words/section/clone/
---
## Section.Clone method

Bu bölümün bir kopyasını oluşturur.

```csharp
public Section Clone()
```

## Örnekler

Bir belgede bölümlerin nasıl eklenip kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Dokümanın ilk bölümünü silin.
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
