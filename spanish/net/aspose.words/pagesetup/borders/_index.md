---
title: PageSetup.Borders
second_title: Referencia de API de Aspose.Words para .NET
description: PageSetup propiedad. Obtiene una colección de los bordes de la página.
type: docs
weight: 50
url: /es/net/aspose.words/pagesetup/borders/
---
## PageSetup.Borders property

Obtiene una colección de los bordes de la página.

```csharp
public BorderCollection Borders { get; }
```

### Ejemplos

Muestra cómo crear un borde de página verde ondulado con una sombra.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### Ver también

* class [BorderCollection](../../bordercollection/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../pagesetup/)
* asamblea [Aspose.Words](../../../)


