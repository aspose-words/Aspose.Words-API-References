---
title: ShapeBase.HorizontalAlignment
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShapeBase HorizontalAlignment för att optimera den horisontella placeringen av former i din design för förbättrad layoutkontroll.
type: docs
weight: 240
url: /sv/net/aspose.words.drawing/shapebase/horizontalalignment/
---
## ShapeBase.HorizontalAlignment property

Anger hur formen placeras horisontellt.

```csharp
public HorizontalAlignment HorizontalAlignment { get; set; }
```

## Anmärkningar

Standardvärdet ärNone.

Har endast effekt för flytande former på översta nivån.

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

* enum [HorizontalAlignment](../../horizontalalignment/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
