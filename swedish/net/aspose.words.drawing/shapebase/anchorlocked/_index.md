---
title: ShapeBase.AnchorLocked
linktitle: AnchorLocked
articleTitle: AnchorLocked
second_title: Aspose.Words för .NET
description: ShapeBase AnchorLocked fast egendom. Anger om formens ankare är låst i C#.
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

Har effekt endast för former på högsta nivå.

Den här egenskapen påverkar beteendet hos formens ankare i Microsoft Word. När ankaret inte är låst, kan flytta formens ankare också flytta formen i Microsoft Word.

## Exempel

Visar hur du låser eller låser upp en forms styckeankare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// Ställ in egenskapen "AnchorLocked" till "true" för att förhindra formens ankare
// från att flyttas när formen flyttas i Microsoft Word.
// Ställ in egenskapen "AnchorLocked" till "false" för att tillåta alla rörelser av formen
// för att också flytta dess ankare till ett annat stycke som formen hamnar nära.
shape.AnchorLocked = anchorLocked;

// Om formen inte har en synlig ankarsymbol till vänster,
// vi kommer att behöva aktivera synliga ankare via "Alternativ" -> "Visa" -> "Objektankare".
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
