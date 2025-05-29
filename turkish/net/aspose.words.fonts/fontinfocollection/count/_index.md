---
title: FontInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: .NET için Aspose.Words
description: FontInfoCollection Count özelliğini keşfedin, kusursuz veri yönetimi için koleksiyonunuzdaki toplam öğe sayısını zahmetsizce alın.
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/fontinfocollection/count/
---
## FontInfoCollection.Count property

Koleksiyonda bulunan öğelerin sayısını alır.

```csharp
public int Count { get; }
```

## Örnekler

Boş belgede bulunan yazı tipleri hakkında bilgi gösterir.

```csharp
Document doc = new Document();

// Boş bir belge 3 varsayılan yazı tipi içerir. Belgedeki her yazı tipi
// o font hakkında detayları içeren karşılık gelen bir FontInfo nesnesi olacaktır.
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### Ayrıca bakınız

* class [FontInfoCollection](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
