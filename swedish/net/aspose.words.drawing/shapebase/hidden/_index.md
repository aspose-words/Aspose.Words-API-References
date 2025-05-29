---
title: ShapeBase.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words för .NET
description: Styr formens synlighet med ShapeBases hidden-egenskap. Växla enkelt mellan synlig och dold för ökad designflexibilitet.
type: docs
weight: 230
url: /sv/net/aspose.words.drawing/shapebase/hidden/
---
## ShapeBase.Hidden property

Hämtar eller ställer in ett booleskt värde som anger om formen är synlig.

```csharp
public bool Hidden { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` .

## Exempel

Visar hur man döljer formen.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
if (!shape.Hidden)
    shape.Hidden = true;

doc.Save(ArtifactsDir + "Shape.Hidden.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
