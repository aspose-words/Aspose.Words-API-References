---
title: WarningInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få enkelt tillgång till specifika WarningInfoCollection-objekt via index. Effektivisera din datahantering med vår intuitiva egenskapsfunktion!
type: docs
weight: 30
url: /sv/net/aspose.words/warninginfocollection/item/
---
## WarningInfoCollection indexer

Hämtar ett objekt vid det angivna indexet.

```csharp
public WarningInfo this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Nollbaserat index för objektet. |

## Exempel

Visar hur man får varningar om format som inte stöds.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### Se även

* class [WarningInfo](../../warninginfo/)
* class [WarningInfoCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
