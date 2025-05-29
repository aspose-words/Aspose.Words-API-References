---
title: TextPath Class
linktitle: TextPath
articleTitle: TextPath
second_title: Aspose.Words para .NET
description: Descubre la clase Aspose.Words.Drawing.TextPath para crear WordArt impactante. Define fácilmente el texto y el formato para mejorar tus documentos.
type: docs
weight: 1760
url: /es/net/aspose.words.drawing/textpath/
---
## TextPath class

Define el texto y el formato de la ruta de texto (de un objeto de WordArt).

Para obtener más información, visite el[Trabajando con formas](https://docs.aspose.com/words/net/working-with-shapes/) Artículo de documentación.

```csharp
public class TextPath
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Bold](../../aspose.words.drawing/textpath/bold/) { get; set; } | Verdadero si la fuente está formateada en negrita. |
| [FitPath](../../aspose.words.drawing/textpath/fitpath/) { get; set; } | Define si el texto se ajusta a la ruta de una forma. |
| [FitShape](../../aspose.words.drawing/textpath/fitshape/) { get; set; } | Define si el texto encaja en el cuadro delimitador de una forma. |
| [FontFamily](../../aspose.words.drawing/textpath/fontfamily/) { get; set; } | Define la familia de la fuente textpath. |
| [Italic](../../aspose.words.drawing/textpath/italic/) { get; set; } | Verdadero si la fuente está formateada como cursiva. |
| [Kerning](../../aspose.words.drawing/textpath/kerning/) { get; set; } | Determina si el kerning está activado. |
| [On](../../aspose.words.drawing/textpath/on/) { get; set; } | Define si se muestra el texto. |
| [ReverseRows](../../aspose.words.drawing/textpath/reverserows/) { get; set; } | Determina si el orden de diseño de las filas está invertido. |
| [RotateLetters](../../aspose.words.drawing/textpath/rotateletters/) { get; set; } | Determina si las letras del texto están rotadas. |
| [SameLetterHeights](../../aspose.words.drawing/textpath/sameletterheights/) { get; set; } | Determina si todas las letras tendrán la misma altura independientemente del caso inicial. |
| [Shadow](../../aspose.words.drawing/textpath/shadow/) { get; set; } | Define si se aplica una sombra al texto en una ruta de texto. |
| [Size](../../aspose.words.drawing/textpath/size/) { get; set; } | Define el tamaño de la fuente en puntos. |
| [SmallCaps](../../aspose.words.drawing/textpath/smallcaps/) { get; set; } | Verdadero si la fuente está formateada en mayúsculas pequeñas. |
| [Spacing](../../aspose.words.drawing/textpath/spacing/) { get; set; } | Define la cantidad de espaciado del texto. 1 significa 100%. |
| [StrikeThrough](../../aspose.words.drawing/textpath/strikethrough/) { get; set; } | Verdadero si la fuente está formateada como texto tachado. |
| [Text](../../aspose.words.drawing/textpath/text/) { get; set; } | Define el texto de la ruta de texto. |
| [TextPathAlignment](../../aspose.words.drawing/textpath/textpathalignment/) { get; set; } | Define la alineación del texto. |
| [Trim](../../aspose.words.drawing/textpath/trim/) { get; set; } | Determina si se elimina el espacio adicional encima y debajo del texto. |
| [Underline](../../aspose.words.drawing/textpath/underline/) { get; set; } | Verdadero si la fuente está subrayada. |
| [XScale](../../aspose.words.drawing/textpath/xscale/) { get; set; } | Determina si se utilizará una ruta de texto recta en lugar de la ruta de forma. |

## Observaciones

Utilice el[`TextPath`](../shape/textpath/) propiedad para acceder a las propiedades de WordArt de una forma. No crea instancias de la`TextPath` clase directamente.

## Ejemplos

Muestra cómo trabajar con WordArt.

```csharp
public void InsertTextPaths()
{
    Document doc = new Document();

    // Inserte un objeto WordArt para mostrar texto en una forma que podamos redimensionar y mover usando el mouse en Microsoft Word.
    // Proporcione un "ShapeType" como argumento para establecer una forma para WordArt.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.",
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // Aplique las configuraciones de formato "Negrita" y "Cursiva" al texto utilizando las propiedades respectivas.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // A continuación se muestran otras propiedades relacionadas con el formato de texto.
    Assert.False(shape.TextPath.Underline);
    Assert.False(shape.TextPath.Shadow);
    Assert.False(shape.TextPath.StrikeThrough);
    Assert.False(shape.TextPath.ReverseRows);
    Assert.False(shape.TextPath.XScale);
    Assert.False(shape.TextPath.Trim);
    Assert.False(shape.TextPath.SmallCaps);

    Assert.AreEqual(36.0, shape.TextPath.Size);
    Assert.AreEqual("Hello World! This text is bold, and italic.", shape.TextPath.Text);
    Assert.AreEqual(ShapeType.TextPlainText, shape.ShapeType);

    // Utilice la propiedad "On" para mostrar/ocultar el texto.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // Utilice la propiedad "Kerning" para habilitar o deshabilitar el espaciado entre caracteres entre ciertos caracteres.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // Utilice la propiedad "Espaciado" para establecer el espaciado personalizado entre caracteres en una escala de 0.0 (ninguno) a 1.0 (predeterminado).
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // Establezca la propiedad "RotateLetters" en "true" para rotar cada carácter 90 grados en sentido antihorario.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // Establezca la propiedad "SameLetterHeights" en "true" para que la altura x de cada carácter sea igual a la altura de mayúsculas.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // De forma predeterminada, el tamaño del texto siempre se escalará para adaptarse al tamaño de la forma que lo contiene, anulando la configuración del tamaño del texto.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // Si establecemos la propiedad "FitShape: en "false", el texto mantendrá el tamaño
    // que la propiedad "Tamaño" especifica independientemente del tamaño de la forma.
    // Utilice la propiedad "TextPathAlignment" también para alinear el texto a un lado de la forma.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");
}

/// <summary>
/// Insertar un nuevo párrafo con una forma de WordArt dentro de él.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // Crea una forma en línea, que servirá como contenedor para nuestro WordArt.
    // La forma solo puede ser una forma válida de WordArt si le asignamos un ShapeType designado por WordArt.
    // Estos tipos tendrán "objeto WordArt" en la descripción,
    // y sus nombres de constantes de enumerador comenzarán todos con "Texto".
    Shape shape = new Shape(doc, wordArtShapeType)
    {
        WrapType = WrapType.Inline,
        Width = shapeWidth,
        Height = shapeHeight,
        FillColor = wordArtFill,
        StrokeColor = line
    };

    shape.TextPath.Text = text;
    shape.TextPath.FontFamily = textFontFamily;

    Paragraph para = (Paragraph)doc.FirstSection.Body.AppendChild(new Paragraph(doc));
    para.AppendChild(shape);
    return shape;
}
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
