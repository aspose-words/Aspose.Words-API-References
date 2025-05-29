---
title: Fill.Pattern
linktitle: Pattern
articleTitle: Pattern
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Fyllningsmönster för att enkelt komma åt och anpassa PatternType för dina designer. Förbättra dina projekt med unika fyllningsalternativ!
type: docs
weight: 160
url: /sv/net/aspose.words.drawing/fill/pattern/
---
## Fill.Pattern property

Får en[`PatternType`](../../patterntype/) för fyllningen.

```csharp
public PatternType Pattern { get; }
```

## Exempel

Visar hur man ställer in mönster för en form.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Det finns flera sätt att ange fyllning i ett mönster.
// 1 - Applicera mönster på formfyllningen:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Applicera mönster med förgrunds- och bakgrundsfärger på formfyllningen:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Se även

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
