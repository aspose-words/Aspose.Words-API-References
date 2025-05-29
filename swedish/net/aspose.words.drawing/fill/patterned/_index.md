---
title: Fill.Patterned
linktitle: Patterned
articleTitle: Patterned
second_title: Aspose.Words för .NET
description: Upptäck metoden Fill Patterned för att enkelt applicera unika mönster på dina designer, vilket förbättrar kreativiteten och den visuella attraktionskraften i dina projekt.
type: docs
weight: 230
url: /sv/net/aspose.words.drawing/fill/patterned/
---
## Patterned(*[PatternType](../../patterntype/)*) {#patterned}

Ställer in den angivna fyllningen till ett mönster.

```csharp
public void Patterned(PatternType patternType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |

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

---

## Patterned(*[PatternType](../../patterntype/), Color, Color*) {#patterned_1}

Ställer in den angivna fyllningen till ett mönster.

```csharp
public void Patterned(PatternType patternType, Color foreColor, Color backColor)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |
| foreColor | Color | Färgen på förgrundsfyllningen. |
| backColor | Color | Färgen på bakgrundsfyllningen. |

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
