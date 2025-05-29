---
title: PageSetup.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words para .NET
description: Descubra la propiedad Bordes de PageSetup para acceder y personalizar fácilmente los bordes de su página para lograr una apariencia pulida y profesional en sus documentos.
type: docs
weight: 50
url: /es/net/aspose.words/pagesetup/borders/
---
## PageSetup.Borders property

Obtiene una colección de los bordes de la página.

```csharp
public BorderCollection Borders { get; }
```

## Ejemplos

Muestra cómo crear un borde de página ondulado verde con una sombra.

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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
