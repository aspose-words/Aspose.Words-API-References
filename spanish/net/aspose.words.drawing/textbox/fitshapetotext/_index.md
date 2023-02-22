---
title: TextBox.FitShapeToText
second_title: Referencia de API de Aspose.Words para .NET
description: TextBox propiedad. Determina si Microsoft Word aumentará la forma para que se ajuste al texto.
type: docs
weight: 10
url: /es/net/aspose.words.drawing/textbox/fitshapetotext/
---
## TextBox.FitShapeToText property

Determina si Microsoft Word aumentará la forma para que se ajuste al texto.

```csharp
public bool FitShapeToText { get; set; }
```

### Observaciones

El valor predeterminado es **falso**.

### Ejemplos

Muestra cómo hacer que un cuadro de texto cambie de tamaño para que se ajuste perfectamente a su contenido.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Aplicar estos valores a ambos miembros para que la forma principal se ajuste
// estrechamente alrededor del contenido del texto, ignorando las dimensiones que hemos establecido.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Ver también

* class [TextBox](../)
* espacio de nombres [Aspose.Words.Drawing](../../textbox/)
* asamblea [Aspose.Words](../../../)


