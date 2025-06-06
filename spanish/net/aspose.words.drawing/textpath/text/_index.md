---
title: TextPath.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words para .NET
description: Explore la propiedad Texto de TextPath para definir y personalizar sin esfuerzo sus rutas de texto para obtener efectos visuales sorprendentes en sus diseños.
type: docs
weight: 160
url: /es/net/aspose.words.drawing/textpath/text/
---
## TextPath.Text property

Define el texto de la ruta de texto.

```csharp
public string Text { get; set; }
```

## Observaciones

El valor predeterminado es una cadena vacía.

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

* class [TextPath](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
