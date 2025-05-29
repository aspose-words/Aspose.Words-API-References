---
title: ShapeBase.BehindText
linktitle: BehindText
articleTitle: BehindText
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase BehindText-egenskapen för att styra formlager i dina designer, vilket enkelt förbättrar textens synlighet och layoutens precision.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing/shapebase/behindtext/
---
## ShapeBase.BehindText property

Anger om formen är under eller ovanför texten.

```csharp
public bool BehindText { get; set; }
```

## Anmärkningar

Har endast effekt för former på översta nivån.

Standardvärdet är`falsk`.

## Exempel

Visar hur man infogar en flytande bild i mitten av en sida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en flytande bild som visas bakom den överlappande texten och justera den mot sidans mitt.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
