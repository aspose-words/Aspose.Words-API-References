---
title: TextBox.NoTextRotation
second_title: Aspose.Words för .NET API Referens
description: TextBox fast egendom. Hämtar eller ställer in ett booleskt värde som anger att någon av texterna i TextBox inte ska rotera när formen roteras.
type: docs
weight: 80
url: /sv/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

Hämtar eller ställer in ett booleskt värde som anger att någon av texterna i TextBox inte ska rotera när formen roteras.

```csharp
public bool NoTextRotation { get; set; }
```

### Anmärkningar

Standardvärdet är`falsk`

### Exempel

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
* namnutrymme [Aspose.Words.Drawing](../../textbox/)
* hopsättning [Aspose.Words](../../../)


