---
title: BorderCollection.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words para .NET
description: BorderCollection LineStyle propiedad. Obtiene o establece el estilo del borde en C#.
type: docs
weight: 80
url: /es/net/aspose.words/bordercollection/linestyle/
---
## BorderCollection.LineStyle property

Obtiene o establece el estilo del borde.

```csharp
public LineStyle LineStyle { get; set; }
```

## Observaciones

Devuelve el estilo del primer borde de la colección.

Establece el estilo de todos los bordes de la colección, excepto los bordes diagonales.

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

* enum [LineStyle](../../linestyle/)
* class [BorderCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
