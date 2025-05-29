---
title: ShapeBase.VerticalAlignment
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShapeBase VerticalAlignment för att optimera din forms vertikala positionering för förbättrad designprecision och visuell attraktionskraft.
type: docs
weight: 600
url: /sv/net/aspose.words.drawing/shapebase/verticalalignment/
---
## ShapeBase.VerticalAlignment property

Anger hur formen placeras vertikalt.

```csharp
public VerticalAlignment VerticalAlignment { get; set; }
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

* enum [VerticalAlignment](../../verticalalignment/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
