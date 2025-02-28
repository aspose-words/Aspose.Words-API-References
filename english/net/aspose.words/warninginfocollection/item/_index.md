---
title: WarningInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: Access specific WarningInfoCollection items effortlessly by index. Streamline your data management with our intuitive property feature!
type: docs
weight: 30
url: /net/aspose.words/warninginfocollection/item/
---
## WarningInfoCollection indexer

Gets an item at the specified index.

```csharp
public WarningInfo this[int index] { get; }
```

| Parameter | Description |
| --- | --- |
| index | Zero-based index of the item. |

## Examples

Shows how to get warnings about unsupported formats.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### See Also

* class [WarningInfo](../../warninginfo/)
* class [WarningInfoCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
