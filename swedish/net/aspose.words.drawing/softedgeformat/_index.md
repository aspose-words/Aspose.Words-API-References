---
title: SoftEdgeFormat Class
linktitle: SoftEdgeFormat
articleTitle: SoftEdgeFormat
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.SoftEdgeFormat för att förbättra dina dokument med fantastiska mjuka kanter för ett professionellt utseende.
type: docs
weight: 1710
url: /sv/net/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class

Representerar mjukkantsformatering för ett objekt.

```csharp
public class SoftEdgeFormat
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Radius](../../aspose.words.drawing/softedgeformat/radius/) { get; set; } | Hämtar eller ställer in ett dubbelvärde som representerar längden på radien för en mjuk kanteffekt i punkter (pt). Standardvärdet är 0,0. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Remove](../../aspose.words.drawing/softedgeformat/remove/)() | Tar bort`SoftEdgeFormat` från föräldraobjektet. |

## Anmärkningar

Använd[`SoftEdge`](../shapebase/softedge/) egenskap för att komma åt mjukkantsegenskaper för ett objekt. Du skapar inte instanser av`SoftEdgeFormat` klass direkt.

## Exempel

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

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
