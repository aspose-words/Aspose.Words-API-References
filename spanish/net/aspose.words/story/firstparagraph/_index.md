---
title: Story.FirstParagraph
second_title: Referencia de API de Aspose.Words para .NET
description: Story propiedad. Obtiene el primer párrafo de la historia.
type: docs
weight: 10
url: /es/net/aspose.words/story/firstparagraph/
---
## Story.FirstParagraph property

Obtiene el primer párrafo de la historia.

```csharp
public Paragraph FirstParagraph { get; }
```

### Ejemplos

Muestra cómo dar formato a una tirada de texto utilizando su propiedad de fuente.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* espacio de nombres [Aspose.Words](../../story/)
* asamblea [Aspose.Words](../../../)


