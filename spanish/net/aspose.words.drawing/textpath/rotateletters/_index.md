---
title: TextPath.RotateLetters
second_title: Referencia de API de Aspose.Words para .NET
description: TextPath propiedad. Determina si las letras del texto se rotan.
type: docs
weight: 90
url: /es/net/aspose.words.drawing/textpath/rotateletters/
---
## TextPath.RotateLetters property

Determina si las letras del texto se rotan.

```csharp
public bool RotateLetters { get; set; }
```

### Observaciones

El valor predeterminado es`FALSO`.

### Ejemplos

Muestra cómo trabajar con WordArt.

```csharp
public void InsertTextPaths()
{
    Document doc = new Document();

    // Inserta un objeto de WordArt para mostrar texto en una forma que podamos cambiar de tamaño y mover usando el mouse en Microsoft Word.
    // Proporciona un "ShapeType" como argumento para establecer una forma para WordArt.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.", 
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // Aplique las configuraciones de formato "Negrita" y "Cursiva" al texto usando las propiedades respectivas.
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

    // Utilice la propiedad "Activado" para mostrar/ocultar el texto.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // Utilice la propiedad "Kerning" para habilitar/deshabilitar el espacio entre ciertos caracteres.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // Utilice la propiedad "Espaciado" para establecer el espacio personalizado entre caracteres en una escala de 0,0 (ninguno) a 1,0 (predeterminado).
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // Establece la propiedad "RotateLetters" en "true" para rotar cada carácter 90 grados en sentido antihorario.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // Establece la propiedad "SameLetterHeights" en "true" para que la altura x de cada carácter sea igual a la altura del límite.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // De forma predeterminada, el tamaño del texto siempre se escalará para ajustarse al tamaño de la forma que lo contiene, anulando la configuración del tamaño del texto.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // Si configuramos la propiedad "FitShape: en "false", el texto mantendrá el tamaño
    // que la propiedad "Tamaño" especifica independientemente del tamaño de la forma.
    // Utilice la propiedad "TextPathAlignment" también para alinear el texto a un lado de la forma.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");
}

/// <summary>
/// Inserta un nuevo párrafo con una forma de WordArt en su interior.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // Crea una forma en línea, que servirá como contenedor para nuestro WordArt.
    // La forma solo puede ser una forma válida de WordArt si le asignamos un ShapeType designado por WordArt.
    // Estos tipos tendrán "objeto WordArt" en la descripción,
    // y sus nombres constantes de enumerador comenzarán con "Texto".
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
* espacio de nombres [Aspose.Words.Drawing](../../textpath/)
* asamblea [Aspose.Words](../../../)


