---
title: WarningInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: .NET için Aspose.Words
description: Verimli veri yönetimi için koleksiyonunuzdaki toplam öğe sayısına kolayca erişmek amacıyla WarningInfoCollection Count özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words/warninginfocollection/count/
---
## WarningInfoCollection.Count property

Koleksiyonda bulunan öğelerin sayısını alır.

```csharp
public int Count { get; }
```

## Örnekler

Desteklenmeyen formatlar hakkında uyarıların nasıl alınacağını gösterir.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### Ayrıca bakınız

* class [WarningInfoCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
