---
title: PageSetup.HeaderDistance
linktitle: HeaderDistance
articleTitle: HeaderDistance
second_title: Aspose.Words para .NET
description: Ajuste la propiedad HeaderDistance de PageSetup para personalizar el espaciado del encabezado en puntos, mejorando el diseño de su documento para una mejor legibilidad y presentación.
type: docs
weight: 170
url: /es/net/aspose.words/pagesetup/headerdistance/
---
## PageSetup.HeaderDistance property

Devuelve o establece la distancia (en puntos) entre el encabezado y la parte superior de la página.

```csharp
public double HeaderDistance { get; set; }
```

## Ejemplos

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

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
