---
title: Shape.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words para .NET
description: Recupera el primer párrafo de una forma sin esfuerzo. Mejora el diseño de tu documento con nuestra sencilla función "Primer párrafo de forma".
type: docs
weight: 70
url: /es/net/aspose.words.drawing/shape/firstparagraph/
---
## Shape.FirstParagraph property

Obtiene el primer párrafo de la forma.

```csharp
public Paragraph FirstParagraph { get; }
```

## Ejemplos

Muestra cómo crear y formatear un cuadro de texto.

```csharp
Document doc = new Document();

// Crea un cuadro de texto flotante.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Establezca la alineación horizontal y vertical del texto dentro de la forma.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Agregue un párrafo al cuadro de texto y agregue una serie de texto que mostrará el cuadro de texto.
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
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
