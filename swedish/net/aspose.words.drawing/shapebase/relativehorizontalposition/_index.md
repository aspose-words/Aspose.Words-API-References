---
title: ShapeBase.RelativeHorizontalPosition
linktitle: RelativeHorizontalPosition
articleTitle: RelativeHorizontalPosition
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShapeBase RelativeHorizontalPosition för att bemästra horisontell positionering av former. Optimera din design med precision och kontroll!
type: docs
weight: 450
url: /sv/net/aspose.words.drawing/shapebase/relativehorizontalposition/
---
## ShapeBase.RelativeHorizontalPosition property

Anger i förhållande till vad formen är placerad horisontellt.

```csharp
public RelativeHorizontalPosition RelativeHorizontalPosition { get; set; }
```

## Anmärkningar

Standardvärdet ärColumn.

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

* enum [RelativeHorizontalPosition](../../relativehorizontalposition/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
