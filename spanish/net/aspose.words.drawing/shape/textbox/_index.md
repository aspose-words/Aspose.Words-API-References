---
title: Shape.TextBox
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words para .NET
description: Personaliza las propiedades de tu cuadro de texto de forma para mejorar la visualización del texto y el atractivo visual de tus diseños. ¡Desbloquea tu potencial creativo hoy mismo!
type: docs
weight: 230
url: /es/net/aspose.words.drawing/shape/textbox/
---
## Shape.TextBox property

Define atributos que especifican cómo se muestra el texto en una forma.

```csharp
public TextBox TextBox { get; }
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

* class [TextBox](../../textbox/)
* class [Shape](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
