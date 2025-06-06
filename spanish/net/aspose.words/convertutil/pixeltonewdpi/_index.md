---
title: ConvertUtil.PixelToNewDpi
linktitle: PixelToNewDpi
articleTitle: PixelToNewDpi
second_title: Aspose.Words para .NET
description: Transforme la resolución de píxeles fácilmente con el método PixelToNewDpi de ConvertUtil. Consiga una calidad de imagen y precisión óptimas para sus proyectos.
type: docs
weight: 30
url: /es/net/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil.PixelToNewDpi method

Convierte píxeles de una resolución a otra.

```csharp
public static int PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pixels | Double | El valor a convertir. |
| oldDpi | Double | La resolución actual de dpi (puntos por pulgada). |
| newDpi | Double | La nueva resolución de dpi (puntos por pulgada). |

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
