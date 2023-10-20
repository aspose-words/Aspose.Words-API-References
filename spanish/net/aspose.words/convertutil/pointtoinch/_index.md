---
title: ConvertUtil.PointToInch
linktitle: PointToInch
articleTitle: PointToInch
second_title: Aspose.Words para .NET
description: ConvertUtil PointToInch método. Convierte puntos a pulgadas en C#.
type: docs
weight: 50
url: /es/net/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil.PointToInch method

Convierte puntos a pulgadas.

```csharp
public static double PointToInch(double points)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| points | Double | El valor a convertir. |

## Observaciones

1 pulgada equivale a 72 puntos.

## Ejemplos

Muestra cómo especificar propiedades de página en pulgadas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// La "Configuración de página" de una sección define el tamaño de los márgenes de la página en puntos.
// También podemos usar la clase "ConvertUtil" para usar una unidad de medida más familiar,
// como pulgadas al definir límites.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// Una pulgada son 72 puntos.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// Agregue contenido para demostrar los nuevos márgenes.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### Ver también

* class [ConvertUtil](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
