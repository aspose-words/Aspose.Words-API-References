---
title: Fill.Pattern
linktitle: Pattern
articleTitle: Pattern
second_title: Aspose.Words für .NET
description: Entdecken Sie die Füllmuster-Eigenschaft, um Mustertypen einfach für Ihre Designs anzupassen. Werten Sie Ihre Projekte mit einzigartigen Fülloptionen auf!
type: docs
weight: 160
url: /de/net/aspose.words.drawing/fill/pattern/
---
## Fill.Pattern property

Erhält eine[`PatternType`](../../patterntype/) für die Füllung.

```csharp
public PatternType Pattern { get; }
```

## Beispiele

Zeigt, wie man ein Muster für eine Form festlegt.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Es gibt mehrere Möglichkeiten, ein Muster mit einer bestimmten Füllung zu versehen.
// 1 - Muster auf die Formfüllung anwenden:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Muster mit Vordergrund- und Hintergrundfarben auf die Formfüllung anwenden:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Siehe auch

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
