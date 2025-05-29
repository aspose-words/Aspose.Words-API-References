---
title: FontInfoCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: .NET için Aspose.Words
description: FontInfoCollection'ın isme göre belirli bir font içerip içermediğini keşfedin. Bu temel yöntemle font koleksiyonunuzu kolayca yönetin ve erişin.
type: docs
weight: 60
url: /tr/net/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection.Contains method

Koleksiyonun verilen ada sahip bir yazı tipi içerip içermediğini belirler.

```csharp
public bool Contains(string name)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Bulunacak yazı tipinin büyük/küçük harfe duyarlı olmayan adı. |

### Geri dönüş değeri

`doğru`eğer öğe koleksiyonda bulunursa; aksi takdirde,`YANLIŞ`.

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
