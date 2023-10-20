---
title: TextBox.NoTextRotation
linktitle: NoTextRotation
articleTitle: NoTextRotation
second_title: Aspose.Words para .NET
description: TextBox NoTextRotation propiedad. Obtiene o establece un valor booleano que indica que el texto del cuadro de texto no debe girar cuando se gira la forma en C#.
type: docs
weight: 80
url: /es/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

Obtiene o establece un valor booleano que indica que el texto del cuadro de texto no debe girar cuando se gira la forma.

```csharp
public bool NoTextRotation { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO`

## Ejemplos

Muestra cómo deshabilitar la rotación del texto cuando se gira la forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Ellipse, 20, 20);
shape.TextBox.NoTextRotation = true;

doc.Save(ArtifactsDir + "Shape.NoTextRotation.docx");
```

### Ver también

* class [TextBox](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
