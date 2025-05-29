---
title: TextBox.NoTextRotation
linktitle: NoTextRotation
articleTitle: NoTextRotation
second_title: Aspose.Words för .NET
description: Styr textrotationen i din textruta med egenskapen NoTextRotation. Säkerställ tydlig och läsbar text även när former roteras. Förbättra din design!
type: docs
weight: 80
url: /sv/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

Hämtar eller ställer in ett booleskt värde som anger att någon av texterna i textrutan inte ska rotera när formen roteras.

```csharp
public bool NoTextRotation { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk`

## Exempel

Visar hur man inaktiverar textrotation när formen roteras.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Ellipse, 20, 20);
shape.TextBox.NoTextRotation = true;

doc.Save(ArtifactsDir + "Shape.NoTextRotation.docx");
```

### Se även

* class [TextBox](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
