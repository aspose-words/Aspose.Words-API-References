---
title: ShapeBase.DistanceLeft
linktitle: DistanceLeft
articleTitle: DistanceLeft
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase DistanceLeft-egenskapen för att enkelt justera avståndet i punkter mellan dokumenttexten och den vänstra kanten av former för förbättrad layoutkontroll.
type: docs
weight: 140
url: /sv/net/aspose.words.drawing/shapebase/distanceleft/
---
## ShapeBase.DistanceLeft property

Returnerar eller anger avståndet (i punkter) mellan dokumenttexten och formens vänstra kant.

```csharp
public double DistanceLeft { get; set; }
```

## Anmärkningar

Standardvärdet är 1/8 tum.

Har endast effekt för former på översta nivån.

## Exempel

Visar hur man ställer in radbrytningsavståndet för text som omger en form.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en rektangel och få texten att radbrytas tätt runt dess gränser.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// Ställ in det minsta avståndet mellan formen och den omgivande texten till 40 pt från alla sidor.
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// Flytta formen närmare mitten av sidan och rotera sedan formen 60 grader medurs.
shape.Top = 75;
shape.Left = 150;
shape.Rotation = 60;

// Lägg till text som bryts runt formen.
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
