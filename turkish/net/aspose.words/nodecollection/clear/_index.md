---
title: NodeCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: .NET için Aspose.Words
description: En iyi performansı elde etmek için NodeCollection'ınızı Clear metodumuzla zahmetsizce temizleyin ve hem koleksiyondan hem de belgeden tüm düğümleri kaldırın.
type: docs
weight: 40
url: /tr/net/aspose.words/nodecollection/clear/
---
## NodeCollection.Clear method

Bu koleksiyondan ve belgeden tüm düğümleri kaldırır.

```csharp
public void Clear()
```

## Örnekler

Bir belgeden tüm bölümlerin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Bu belgenin, belgenin tüm içeriğini barındıran ve görüntüleyen birkaç alt düğümü olan bir bölümü vardır.
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// Bölüm koleksiyonunu temizleyerek belgenin tüm alt öğelerini kaldır.
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Ayrıca bakınız

* class [NodeCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
