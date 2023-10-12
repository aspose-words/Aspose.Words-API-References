---
title: FontInfoCollection.Contains
second_title: Aspose.Words for .NET API Referansı
description: FontInfoCollection yöntem. Koleksiyonun verilen adda bir yazı tipi içerip içermediğini belirler.
type: docs
weight: 60
url: /tr/net/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection.Contains method

Koleksiyonun verilen adda bir yazı tipi içerip içermediğini belirler.

```csharp
public bool Contains(string name)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Bulunacak yazı tipinin büyük/küçük harfe duyarlı olmayan adı. |

### Geri dönüş değeri

`doğru` öğe koleksiyonda bulunursa; aksi takdirde,`YANLIŞ`.

### Örnekler

Boş belgede bulunan yazı tipleri hakkındaki bilgileri gösterir.

```csharp
Document doc = new Document();

// Boş bir belgede 3 varsayılan yazı tipi bulunur. Belgedeki her yazı tipi
// o yazı tipiyle ilgili ayrıntıları içeren karşılık gelen bir FontInfo nesnesine sahip olacaktır.
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### Ayrıca bakınız

* class [FontInfoCollection](../)
* ad alanı [Aspose.Words.Fonts](../../fontinfocollection/)
* toplantı [Aspose.Words](../../../)


