---
title: TextBox.InternalMarginLeft
linktitle: InternalMarginLeft
articleTitle: InternalMarginLeft
second_title: Aspose.Words para .NET
description: TextBox InternalMarginLeft propiedad. Especifica el margen interior izquierdo en puntos para una forma en C#.
type: docs
weight: 30
url: /es/net/aspose.words.drawing/textbox/internalmarginleft/
---
## TextBox.InternalMarginLeft property

Especifica el margen interior izquierdo en puntos para una forma.

```csharp
public double InternalMarginLeft { get; set; }
```

## Observaciones

El valor predeterminado es 1/10 de pulgada.

## Ejemplos

Muestra cómo establecer márgenes internos para un cuadro de texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta otro cuadro de texto con márgenes específicos.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

### Ver también

* class [TextBox](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
