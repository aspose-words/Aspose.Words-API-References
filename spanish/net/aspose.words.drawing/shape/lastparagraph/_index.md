---
title: Shape.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words para .NET
description: Acceda a la propiedad LastParagraph para recuperar fácilmente el párrafo final de su forma, mejorando el diseño y la legibilidad de su documento.
type: docs
weight: 130
url: /es/net/aspose.words.drawing/shape/lastparagraph/
---
## Shape.LastParagraph property

Obtiene el último párrafo de la forma.

```csharp
public Paragraph LastParagraph { get; }
```

## Ejemplos

Muestra cómo establecer la orientación del texto dentro de un cuadro de texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Mueva el generador de documentos dentro del TextBox y agregue texto.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Establezca la propiedad "LayoutFlow" para establecer una orientación para el contenido de texto de este cuadro de texto.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Ver también

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
