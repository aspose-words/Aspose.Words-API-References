---
title: Fill.Patterned
linktitle: Patterned
articleTitle: Patterned
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „Gemustert füllen“, um mühelos einzigartige Muster auf Ihre Designs anzuwenden und so die Kreativität und visuelle Attraktivität Ihrer Projekte zu steigern.
type: docs
weight: 230
url: /de/net/aspose.words.drawing/fill/patterned/
---
## Patterned(*[PatternType](../../patterntype/)*) {#patterned}

Legt die angegebene Füllung auf ein Muster fest.

```csharp
public void Patterned(PatternType patternType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |

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

---

## Patterned(*[PatternType](../../patterntype/), Color, Color*) {#patterned_1}

Legt die angegebene Füllung auf ein Muster fest.

```csharp
public void Patterned(PatternType patternType, Color foreColor, Color backColor)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |
| foreColor | Color | Die Farbe der Vordergrundfüllung. |
| backColor | Color | Die Farbe der Hintergrundfüllung. |

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
