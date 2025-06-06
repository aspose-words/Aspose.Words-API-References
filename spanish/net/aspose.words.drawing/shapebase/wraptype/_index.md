---
title: ShapeBase.WrapType
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words para .NET
description: Descubra la propiedad ShapeBase WrapType, controle formas en línea o flotantes y personalice el ajuste de texto para una mayor flexibilidad de diseño.
type: docs
weight: 640
url: /es/net/aspose.words.drawing/shapebase/wraptype/
---
## ShapeBase.WrapType property

Define si la forma es en línea o flotante. Para las formas flotantes, define el modo de ajuste del texto alrededor de la forma.

```csharp
public WrapType WrapType { get; set; }
```

## Observaciones

El valor predeterminado esNone.

Tiene efecto sólo para formas de nivel superior.

## Ejemplos

Muestra cómo insertar una imagen flotante en el centro de una página.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una imagen flotante que aparecerá detrás del texto superpuesto y la alinea con el centro de la página.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
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

* enum [WrapType](../../wraptype/)
* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
