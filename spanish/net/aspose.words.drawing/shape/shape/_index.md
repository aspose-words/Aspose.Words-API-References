---
title: Shape
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words para .NET
description: Crea objetos con formas únicas sin esfuerzo con nuestro Constructor de Formas. ¡Diseña formas personalizadas y mejora tus proyectos con facilidad y precisión!
type: docs
weight: 10
url: /es/net/aspose.words.drawing/shape/shape/
---
## Shape constructor

Crea un nuevo objeto de forma.

```csharp
public Shape(DocumentBase doc, ShapeType shapeType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |
| shapeType | ShapeType | El tipo de forma a crear. |

## Observaciones

Debes especificar las propiedades de forma deseadas después de crear una forma.

## Ejemplos

Muestra cómo insertar una forma con una imagen del sistema de archivos local en un documento.

```csharp
Document doc = new Document();

// El constructor público de la clase "Shape" creará una forma con el tipo de marcado "ShapeMarkupLanguage.Vml".
// Si necesita crear una forma de un tipo no primitivo, como SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// EsquinasSuperioresUnaRedondeadaUnaRecortada, EsquinaSimpleRedondeada, EsquinasSuperioresRedondeadas o EsquinasDiagonalesRedondeadas
// utilice DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [ShapeType](../../shapetype/)
* class [Shape](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
