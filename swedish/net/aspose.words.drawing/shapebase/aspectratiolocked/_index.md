---
title: ShapeBase.AspectRatioLocked
linktitle: AspectRatioLocked
articleTitle: AspectRatioLocked
second_title: Aspose.Words för .NET
description: ShapeBase AspectRatioLocked fast egendom. Anger om formens bildförhållande är låst i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## ShapeBase.AspectRatioLocked property

Anger om formens bildförhållande är låst.

```csharp
public bool AspectRatioLocked { get; set; }
```

## Anmärkningar

Standardvärdet beror på[`ShapeType`](../../shapetype/) , förImage det är`Sann` men för de andra formtyperna är det`falsk`.

Har effekt endast för former på toppnivå.

## Exempel

Visar hur man låser/låser upp en forms bildförhållande.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en form. Om vi öppnar det här dokumentet i Microsoft Word kan vi vänsterklicka på formen för att avslöja
// åtta storlekshandtag runt dess omkrets, som vi kan klicka och dra för att ändra storleken.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Ställ in egenskapen "AspectRatioLocked" till "true" för att bevara formens bildförhållande
// när du använder något av de fyra diagonala storlekshandtagen, som ändrar både bildens höjd och bredd.
// Att använda alla ortogonala storlekshandtag som antingen ändrar höjden eller bredden kommer fortfarande att ändra bildförhållandet.
// Ställ in egenskapen "AspectRatioLocked" till "false" för att tillåta oss
// ändra fritt bildens bildförhållande med alla storlekshandtag.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
