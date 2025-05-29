---
title: SoftEdgeFormat.Radius
linktitle: Radius
articleTitle: Radius
second_title: Aspose.Words för .NET
description: Upptäck SoftEdgeFormat Radius-egenskapen för att enkelt justera mjuka kanter. Kontrollera radielängden med precision för fantastiska visuella resultat.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing/softedgeformat/radius/
---
## SoftEdgeFormat.Radius property

Hämtar eller ställer in ett dubbelvärde som representerar längden på radien för en mjuk kanteffekt i punkter (pt). Standardvärdet är 0,0.

```csharp
public double Radius { get; set; }
```

## Exempel

Visar hur man ställer in en gräns för bildupplösning.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

Visar hur man arbetar med mjuka kanter.

```csharp
DocumentBuilder builder = new DocumentBuilder();
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 200);

// Applicera en mjuk kant på formen.
shape.SoftEdge.Radius = 30;

builder.Document.Save(ArtifactsDir + "Shape.SoftEdge.docx");

// Ladda dokument med rektangulär form med mjuk kant.
Document doc = new Document(ArtifactsDir + "Shape.SoftEdge.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
SoftEdgeFormat softEdgeFormat = shape.SoftEdge;

// Kontrollera mjukkantens radie.
Assert.AreEqual(30, softEdgeFormat.Radius);

// Ta bort den mjuka kanten från formen.
softEdgeFormat.Remove();

// Kontrollera radien på den borttagna mjuka kanten.
Assert.AreEqual(0, softEdgeFormat.Radius);
```

### Se även

* class [SoftEdgeFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
