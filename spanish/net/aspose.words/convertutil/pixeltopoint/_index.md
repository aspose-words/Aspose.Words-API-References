---
title: ConvertUtil.PixelToPoint
linktitle: PixelToPoint
articleTitle: PixelToPoint
second_title: Aspose.Words para .NET
description: Convierte píxeles a puntos a 96 ppp sin esfuerzo con el método PixelToPoint de ConvertUtil. ¡Mejora la precisión de tus diseños hoy mismo!
type: docs
weight: 40
url: /es/net/aspose.words/convertutil/pixeltopoint/
---
## PixelToPoint(*double*) {#pixeltopoint}

Convierte píxeles en puntos a 96 dpi.

```csharp
public static double PixelToPoint(double pixels)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pixels | Double | El valor a convertir. |

## Observaciones

1 pulgada equivale a 72 puntos.

## Ejemplos

Muestra cómo especificar las propiedades de la página en píxeles.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//La "Configuración de página" de una sección define el tamaño de los márgenes de la página en puntos.
// También podemos usar la clase "ConvertUtil" para utilizar una unidad de medida diferente,
// como los píxeles al definir límites.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100);
pageSetup.BottomMargin = ConvertUtil.PixelToPoint(200);
pageSetup.LeftMargin = ConvertUtil.PixelToPoint(225);
pageSetup.RightMargin = ConvertUtil.PixelToPoint(125);

//Un píxel son 0,75 puntos.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToPixel(0.75));

//El valor de DPI predeterminado utilizado es 96.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1, 96));

//Añadir contenido para demostrar los nuevos márgenes.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToPixel(pageSetup.LeftMargin)} pixels from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToPixel(pageSetup.RightMargin)} pixels from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin)} pixels from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToPixel(pageSetup.BottomMargin)} pixels from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixels.docx");
```

### Ver también

* class [ConvertUtil](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## PixelToPoint(*double, double*) {#pixeltopoint_1}

Convierte píxeles en puntos con la resolución de píxeles especificada.

```csharp
public static double PixelToPoint(double pixels, double resolution)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pixels | Double | El valor a convertir. |
| resolution | Double | La resolución de dpi (puntos por pulgada). |

## Observaciones

1 pulgada equivale a 72 puntos.

## Ejemplos

Muestra cómo utilizar la conversión de puntos a píxeles con resolución predeterminada y personalizada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Define el tamaño del margen superior de esta sección en píxeles, de acuerdo con un DPI personalizado.
const double myDpi = 192;

PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100, myDpi);

Assert.AreEqual(37.5d, pageSetup.TopMargin, 0.01d);

// Con el DPI predeterminado de 96, un píxel equivale a 0,75 puntos.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));

builder.Writeln($"This Text is {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                $"pixels (at a DPI of {myDpi}) from the top of the page.");

// Establezca un nuevo DPI y ajuste el valor del margen superior en consecuencia.
const double newDpi = 300;
pageSetup.TopMargin = ConvertUtil.PixelToNewDpi(pageSetup.TopMargin, myDpi, newDpi);
Assert.AreEqual(59.0d, pageSetup.TopMargin, 0.01d);

builder.Writeln($"At a DPI of {newDpi}, the text is now {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                "pixels from the top of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixelsDpi.docx");
```

### Ver también

* class [ConvertUtil](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
