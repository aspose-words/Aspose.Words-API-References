---
title: TextBox.LayoutFlow
second_title: Referencia de API de Aspose.Words para .NET
description: TextBox propiedad. Determina el flujo del diseño del texto en una forma.
type: docs
weight: 60
url: /es/net/aspose.words.drawing/textbox/layoutflow/
---
## TextBox.LayoutFlow property

Determina el flujo del diseño del texto en una forma.

```csharp
public LayoutFlow LayoutFlow { get; set; }
```

### Observaciones

El valor predeterminado esHorizontal.

### Ejemplos

Muestra cómo establecer la orientación del texto dentro de un cuadro de texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Mueva el generador de documentos al interior del cuadro de texto y agregue texto.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Establece la propiedad "LayoutFlow" para establecer una orientación para el contenido del texto de este cuadro de texto.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Ver también

* enum [LayoutFlow](../../layoutflow/)
* class [TextBox](../)
* espacio de nombres [Aspose.Words.Drawing](../../textbox/)
* asamblea [Aspose.Words](../../../)


