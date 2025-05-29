---
title: Adjustment Class
linktitle: Adjustment
articleTitle: Adjustment
second_title: .NET için Aspose.Words
description: Üstün belge biçimlendirme için şekillerinizi hassas ayarlama değerleriyle geliştirmek üzere tasarlanmış Aspose.Words.Drawing.Adjustment sınıfını keşfedin.
type: docs
weight: 700
url: /tr/net/aspose.words.drawing/adjustment/
---
## Adjustment class

Belirtilen şekle uygulanan ayar değerlerini temsil eder.

```csharp
public class Adjustment
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Name](../../aspose.words.drawing/adjustment/name/) { get; } | Ayarlamanın adını alır. |
| [Value](../../aspose.words.drawing/adjustment/value/) { get; set; } | Ayarlamanın ham değerini alır veya ayarlar. |

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
