---
title: NodeCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: .NET için Aspose.Words
description: NodeCollection RemoveAt yöntemiyle koleksiyonunuzdan düğümleri zahmetsizce kaldırın. Belirli düğümleri hızla kaldırarak belge yönetimini kolaylaştırın.
type: docs
weight: 100
url: /tr/net/aspose.words/nodecollection/removeat/
---
## NodeCollection.RemoveAt method

Belirtilen dizindeki düğümü koleksiyondan ve belgeden kaldırır.

```csharp
public void RemoveAt(int index)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Düğümün sıfırdan başlayan indeksi. Negatif indekslere izin verilir ve listenin sonundan erişimi belirtir. Örneğin -1 son düğüm anlamına gelir, -2 sondan bir önceki düğüm anlamına gelir, vb. |

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

* class [NodeCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
