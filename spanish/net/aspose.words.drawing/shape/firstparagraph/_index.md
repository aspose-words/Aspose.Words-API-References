---
title: Shape.FirstParagraph
second_title: Referencia de API de Aspose.Words para .NET
description: Shape propiedad. Obtiene el primer párrafo de la forma.
type: docs
weight: 60
url: /es/net/aspose.words.drawing/shape/firstparagraph/
---
## Shape.FirstParagraph property

Obtiene el primer párrafo de la forma.

```csharp
public Paragraph FirstParagraph { get; }
```

### Ejemplos

Muestra cómo crear y dar formato a un cuadro de texto.

```csharp
Document doc = new Document();

// Crea un cuadro de texto flotante.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Establecer la alineación horizontal y vertical del texto dentro de la forma.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Agregue un párrafo al cuadro de texto y agregue una secuencia de texto que se mostrará en el cuadro de texto.
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### Ver también

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* espacio de nombres [Aspose.Words.Drawing](../../shape/)
* asamblea [Aspose.Words](../../../)


