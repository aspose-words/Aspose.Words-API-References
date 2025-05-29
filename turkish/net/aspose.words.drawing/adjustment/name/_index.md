---
title: Adjustment.Name
linktitle: Name
articleTitle: Name
second_title: .NET için Aspose.Words
description: Gelişmiş verimlilik ve akıcı iş akışları için ayarlamalarınıza kolayca erişmek ve bunları yönetmek amacıyla Ayarlama Adı özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing/adjustment/name/
---
## Adjustment.Name property

Ayarlamanın adını alır.

```csharp
public string Name { get; }
```

## Örnekler

Ayarlama ham değerleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rounded rectangle shape.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

AdjustmentCollection adjustments = shape.Adjustments;
Assert.AreEqual(1, adjustments.Count);

Adjustment adjustment = adjustments[0];
Assert.AreEqual("adj", adjustment.Name);
Assert.AreEqual(16667, adjustment.Value);

adjustment.Value = 30000;

doc.Save(ArtifactsDir + "Shape.Adjustments.docx");
```

### Ayrıca bakınız

* class [Adjustment](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
