---
title: Fill.Pattern
linktitle: Pattern
articleTitle: Pattern
second_title: .NET için Aspose.Words
description: Tasarımlarınız için PatternType'a kolayca erişmek ve özelleştirmek için Fill Pattern özelliğini keşfedin. Projelerinizi benzersiz dolgu seçenekleriyle geliştirin!
type: docs
weight: 160
url: /tr/net/aspose.words.drawing/fill/pattern/
---
## Fill.Pattern property

Bir tane alır[`PatternType`](../../patterntype/) dolgu için.

```csharp
public PatternType Pattern { get; }
```

## Örnekler

Bir şekle ait desenin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Bir deseni belirtilen dolguyla doldurmanın birkaç yolu vardır.
// 1 - Şekil dolgusuna desen uygula:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Şekil dolgusuna ön plan ve arka plan renkleriyle desen uygula:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Ayrıca bakınız

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
