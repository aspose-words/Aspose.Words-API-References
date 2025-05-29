---
title: ShapeBase.AnchorLocked
linktitle: AnchorLocked
articleTitle: AnchorLocked
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase AnchorLocked-egenskapen för att styra ankarlåsning för former, vilket förbättrar designstabilitet och flexibilitet i dina projekt.
type: docs
weight: 30
url: /sv/net/aspose.words.drawing/shapebase/anchorlocked/
---
## ShapeBase.AnchorLocked property

Anger om formens ankare är låst.

```csharp
public bool AnchorLocked { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk`.

Har endast effekt för former på översta nivån.

Den här egenskapen påverkar beteendet hos formens ankare i Microsoft Word. När ankaret inte är låst kan det även flytta formens ankare i Microsoft Word.

## Exempel

Visar hur man låser eller låser upp en forms styckeankare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// Sätt egenskapen "AnchorLocked" till "true" för att förhindra att formens ankare
// från att flyttas när formen flyttas i Microsoft Word.
// Sätt egenskapen "AnchorLocked" till "false" för att tillåta all förflyttning av formen
// för att även flytta dess ankare till ett annat stycke som formen hamnar nära.
shape.AnchorLocked = anchorLocked;

// Om formen inte har en synlig ankarsymbol till vänster,
// vi måste aktivera synliga ankare via "Alternativ" -> "Visa" -> "Objektankare".
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
