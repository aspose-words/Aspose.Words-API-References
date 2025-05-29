---
title: Shape.HasSmartArt
linktitle: HasSmartArt
articleTitle: HasSmartArt
second_title: .NET için Aspose.Words
description: Shape'inizin HasSmartArt özelliğine sahip bir SmartArt nesnesi içerip içermediğini keşfedin. Projeleriniz için yaratıcı tasarım olanaklarının kilidini açın!
type: docs
weight: 100
url: /tr/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

Geri Döndürür`doğru` eğer bu[`Shape`](../) bir SmartArt nesnesi var.

```csharp
public bool HasSmartArt { get; }
```

## Örnekler

SmartArt nesneleriyle bir belgedeki şekil sayısının nasıl sayılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### Ayrıca bakınız

* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
