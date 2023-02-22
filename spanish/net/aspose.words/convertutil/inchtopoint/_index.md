---
title: ConvertUtil.InchToPoint
second_title: Referencia de API de Aspose.Words para .NET
description: ConvertUtil método. Convierte pulgadas a puntos.
type: docs
weight: 10
url: /es/net/aspose.words/convertutil/inchtopoint/
---
## ConvertUtil.InchToPoint method

Convierte pulgadas a puntos.

```csharp
public static double InchToPoint(double inches)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inches | Double | El valor a convertir. |

### Observaciones

1 pulgada equivale a 72 puntos.

### Ejemplos

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes y otras configuraciones para una sección.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

Muestra cómo especificar las propiedades de la página en pulgadas.

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
* espacio de nombres [Aspose.Words](../../convertutil/)
* asamblea [Aspose.Words](../../../)


