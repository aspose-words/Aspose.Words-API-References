---
title: Fill Class
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words para .NET
description: Explore la clase Aspose.Words.Drawing.Fill para obtener opciones de formato de relleno avanzadas y mejorar el diseño y el atractivo visual de su documento sin esfuerzo.
type: docs
weight: 1270
url: /es/net/aspose.words.drawing/fill/
---
## Fill class

Representa el formato de relleno de un objeto.

Para obtener más información, visite el[Trabajar con elementos gráficos](https://docs.aspose.com/words/net/working-with-graphic-elements/) Artículo de documentación.

```csharp
public class Fill
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | Obtiene o establece un objeto Color que representa el color de fondo para el relleno. |
| [BackThemeColor](../../aspose.words.drawing/fill/backthemecolor/) { get; set; } | Obtiene o establece un objeto ThemeColor que representa el color de fondo para el relleno. |
| [BackTintAndShade](../../aspose.words.drawing/fill/backtintandshade/) { get; set; } | Obtiene o establece un valor doble que aclara u oscurece el color de fondo. |
| [BaseForeColor](../../aspose.words.drawing/fill/baseforecolor/) { get; } | Obtiene un objeto Color que representa el color de primer plano base para el relleno sin ningún modificador. |
| [Color](../../aspose.words.drawing/fill/color/) { get; set; } | Obtiene o establece un objeto Color que representa el color de primer plano para el relleno. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | Obtiene un tipo de relleno. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | Obtiene o establece un objeto Color que representa el color de primer plano para el relleno. |
| [ForeThemeColor](../../aspose.words.drawing/fill/forethemecolor/) { get; set; } | Obtiene o establece un objeto ThemeColor que representa el color de primer plano para el relleno. |
| [ForeTintAndShade](../../aspose.words.drawing/fill/foretintandshade/) { get; set; } | Obtiene o establece un valor doble que aclara u oscurece el color de primer plano. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | Obtiene o establece el ángulo del relleno degradado. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | Obtiene una colección de[`GradientStop`](../gradientstop/) objetos para el relleno. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | Obtiene el estilo de degradado[`GradientStyle`](../gradientstyle/) para el relleno. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | Obtiene la variante de degradado[`GradientVariant`](../gradientvariant/) para el relleno. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | Obtiene los bytes sin procesar de la textura o patrón de relleno. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | Obtiene o establece el grado de opacidad del relleno especificado como un valor entre 0,0 (transparente) y 1,0 (opaco). |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | Obtiene un[`PatternType`](../patterntype/) para el relleno. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | Obtiene un[`PresetTexture`](../presettexture/) para el relleno. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | Obtiene o establece si el relleno gira con el objeto especificado. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | Obtiene o establece la alineación para el relleno de textura de mosaico. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | Obtiene o establece el grado de transparencia del relleno especificado como un valor entre 0,0 (opaco) y 1,0 (transparente). |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | Obtiene o establece el valor que es`verdadero` Si el formato aplicado a esta instancia es visible. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | Establece el relleno especificado en un degradado de un solo color. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(*Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | Establece el relleno especificado en un degradado de un solo color utilizando el color especificado. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(*[PatternType](../patterntype/)*) | Establece el relleno especificado en un patrón. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(*[PatternType](../patterntype/), Color, Color*) | Establece el relleno especificado en un patrón. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(*[PresetTexture](../presettexture/)*) | Establece el relleno en una textura preestablecida. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(*byte[]*) | Cambia el tipo de relleno a una sola imagen. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(*Stream*) | Cambia el tipo de relleno a una sola imagen. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(*string*) | Cambia el tipo de relleno a una sola imagen. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | Establece el relleno en un color uniforme. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(*Color*) | Establece el relleno en un color uniforme especificado. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | Establece el relleno especificado en un degradado de dos colores. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(*Color, Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | Establece el relleno especificado en un degradado de dos colores. |

## Observaciones

Utilice el[`Fill`](../shapebase/fill/) o[`Fill`](../../aspose.words/font/fill/) propiedad para acceder a las propiedades de relleno de un objeto. No crea instancias de la`Fill` clase directamente.

## Ejemplos

Muestra cómo rellenar una forma con un color sólido.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Escribe un texto y luego cúbrelo con una forma flotante.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Utilice la propiedad "StrokeColor" para establecer el color del contorno de la forma.
shape.StrokeColor = Color.CadetBlue;

// Utilice la propiedad "FillColor" para establecer el color del área interior de la forma.
shape.FillColor = Color.LightBlue;

// La propiedad "Opacidad" determina qué tan transparente es el color en una escala de 0 a 1,
// siendo 1 completamente opaco y 0 invisible.
//El relleno de la forma por defecto es totalmente opaco, por lo que no podemos ver el texto sobre el que se encuentra esta forma.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Establezca la opacidad del color de relleno de la forma en un valor más bajo para que podamos ver el texto debajo de él.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
