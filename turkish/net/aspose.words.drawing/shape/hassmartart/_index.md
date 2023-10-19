---
title: Shape.HasSmartArt
linktitle: HasSmartArt
articleTitle: HasSmartArt
second_title: Aspose.Words for .NET
description: Shape HasSmartArt mülk. İadelerdoğru Eğer buShape bir SmartArt nesnesi var C#'da.
type: docs
weight: 90
url: /tr/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

İadeler`doğru` Eğer bu[`Shape`](../) bir SmartArt nesnesi var.

```csharp
public bool HasSmartArt { get; }
```

## Örnekler

SmartArt nesneleri içeren bir belgedeki şekillerin sayısının nasıl sayılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### Ayrıca bakınız

* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
