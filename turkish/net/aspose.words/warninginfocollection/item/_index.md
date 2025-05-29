---
title: WarningInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: Belirli WarningInfoCollection öğelerine dizine göre zahmetsizce erişin. Sezgisel özellik özelliğimizle veri yönetiminizi kolaylaştırın!
type: docs
weight: 30
url: /tr/net/aspose.words/warninginfocollection/item/
---
## WarningInfoCollection indexer

Belirtilen dizindeki bir öğeyi alır.

```csharp
public WarningInfo this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Öğenin sıfırdan başlayan indeksi. |

## Örnekler

Desteklenmeyen formatlar hakkında uyarıların nasıl alınacağını gösterir.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### Ayrıca bakınız

* class [WarningInfo](../../warninginfo/)
* class [WarningInfoCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
