---
title: PageSetup.TopMargin
linktitle: TopMargin
articleTitle: TopMargin
second_title: Aspose.Words para .NET
description: Ajuste la propiedad PageSetup TopMargin para personalizar la distancia desde el borde superior de la página hasta el texto, mejorando el diseño y la legibilidad.
type: docs
weight: 440
url: /es/net/aspose.words/pagesetup/topmargin/
---
## PageSetup.TopMargin property

Devuelve o establece la distancia (en puntos) entre el borde superior de la página y el límite superior del cuerpo del texto.

```csharp
public double TopMargin { get; set; }
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
