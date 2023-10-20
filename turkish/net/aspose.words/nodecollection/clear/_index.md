---
title: NodeCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words for .NET
description: NodeCollection Clear yöntem. Tüm düğümleri bu koleksiyondan ve belgeden kaldırır C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words/nodecollection/clear/
---
## NodeCollection.Clear method

Tüm düğümleri bu koleksiyondan ve belgeden kaldırır.

```csharp
public void Clear()
```

## Örnekler

Bir belgedeki tüm bölümlerin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Bu belgede, belgenin tüm içeriğini içeren ve görüntüleyen birkaç alt düğümün bulunduğu bir bölüm vardır.
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// Belgenin tüm alt öğelerini kaldıracak olan bölüm koleksiyonunu temizleyin.
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Ayrıca bakınız

* class [NodeCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
