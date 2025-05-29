---
title: WarningInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Greifen Sie mühelos per Index auf bestimmte WarningInfoCollection-Elemente zu. Optimieren Sie Ihr Datenmanagement mit unserer intuitiven Eigenschaftenfunktion!
type: docs
weight: 30
url: /de/net/aspose.words/warninginfocollection/item/
---
## WarningInfoCollection indexer

Ruft ein Element am angegebenen Index ab.

```csharp
public WarningInfo this[int index] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Nullbasierter Index des Elements. |

## Beispiele

Zeigt, wie Sie Warnungen zu nicht unterstützten Formaten erhalten.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### Siehe auch

* class [WarningInfo](../../warninginfo/)
* class [WarningInfoCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
