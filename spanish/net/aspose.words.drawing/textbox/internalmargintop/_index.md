---
title: TextBox.InternalMarginTop
linktitle: InternalMarginTop
articleTitle: InternalMarginTop
second_title: Aspose.Words para .NET
description: Descubra la propiedad TextBox InternalMarginTop: controle el margen superior de su forma en puntos para lograr un diseño preciso y una mayor flexibilidad.
type: docs
weight: 50
url: /es/net/aspose.words.drawing/textbox/internalmargintop/
---
## TextBox.InternalMarginTop property

Especifica el margen superior interno en puntos para una forma.

```csharp
public double InternalMarginTop { get; set; }
```

## Observaciones

El valor predeterminado es 1/20 de pulgada.

## Ejemplos

Muestra cómo establecer márgenes internos para un cuadro de texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar otro cuadro de texto con márgenes específicos.
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
