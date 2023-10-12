---
title: TextBox.NoTextRotation
second_title: Aspose.Words für .NET-API-Referenz
description: TextBox eigendom. Ruft einen booleschen Wert ab oder legt diesen fest der angibt dass sich der Text der TextBox nicht drehen soll wenn die Form gedreht wird.
type: docs
weight: 80
url: /de/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, dass sich der Text der TextBox nicht drehen soll, wenn die Form gedreht wird.

```csharp
public bool NoTextRotation { get; set; }
```

### Bemerkungen

Der Standardwert ist`FALSCH`

### Beispiele

Zeigt, wie die Textdrehung deaktiviert wird, wenn die Form gedreht wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Ellipse, 20, 20);
shape.TextBox.NoTextRotation = true;

doc.Save(ArtifactsDir + "Shape.NoTextRotation.docx");
```

### Siehe auch

* class [TextBox](../)
* namensraum [Aspose.Words.Drawing](../../textbox/)
* Montage [Aspose.Words](../../../)


