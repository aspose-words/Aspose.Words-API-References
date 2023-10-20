---
title: ConvertUtil.MillimeterToPoint
linktitle: MillimeterToPoint
articleTitle: MillimeterToPoint
second_title: Aspose.Words para .NET
description: ConvertUtil MillimeterToPoint método. Convierte milímetros a puntos en C#.
type: docs
weight: 20
url: /es/net/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil.MillimeterToPoint method

Convierte milímetros a puntos.

```csharp
public static double MillimeterToPoint(double millimeters)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| millimeters | Double | El valor a convertir. |

## Observaciones

1 pulgada equivale a 25,4 milímetros. 1 pulgada equivale a 72 puntos.

## Ejemplos

Muestra cómo especificar propiedades de página en milímetros.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// La "Configuración de página" de una sección define el tamaño de los márgenes de la página en puntos.
// También podemos usar la clase "ConvertUtil" para usar una unidad de medida más familiar,
// como milímetros al definir límites.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.MillimeterToPoint(30);
pageSetup.BottomMargin = ConvertUtil.MillimeterToPoint(50);
pageSetup.LeftMargin = ConvertUtil.MillimeterToPoint(80);
pageSetup.RightMargin = ConvertUtil.MillimeterToPoint(40);

// Un centímetro equivale aproximadamente a 28,3 puntos.
Assert.AreEqual(28.34d, ConvertUtil.MillimeterToPoint(10), 0.01d);

// Agregue contenido para demostrar los nuevos márgenes.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points from the left, " +
                $"{pageSetup.RightMargin} points from the right, " +
                $"{pageSetup.TopMargin} points from the top, " +
                $"and {pageSetup.BottomMargin} points from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndMillimeters.docx");
```

### Ver también

* class [ConvertUtil](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
