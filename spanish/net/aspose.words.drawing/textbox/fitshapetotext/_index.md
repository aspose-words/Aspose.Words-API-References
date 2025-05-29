---
title: TextBox.FitShapeToText
linktitle: FitShapeToText
articleTitle: FitShapeToText
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad FitShapeToText de Microsoft Word ajusta automáticamente las formas para que se ajusten perfectamente a su texto, mejorando la presentación del documento.
type: docs
weight: 10
url: /es/net/aspose.words.drawing/textbox/fitshapetotext/
---
## TextBox.FitShapeToText property

Determina si Microsoft Word ampliará la forma para que se ajuste al texto.

```csharp
public bool FitShapeToText { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO`.

## Ejemplos

Muestra cómo lograr que un cuadro de texto cambie de tamaño para ajustarse perfectamente a su contenido.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Aplique estos valores a ambos miembros para que la forma principal se ajuste
// firmemente alrededor del contenido del texto, ignorando las dimensiones que hemos establecido.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Ver también

* class [TextBox](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
