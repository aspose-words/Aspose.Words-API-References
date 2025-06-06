---
title: BorderCollection.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words para .NET
description: Descubre la propiedad Sombra de BorderCollection para realzar tus diseños. ¡Controla fácilmente las sombras de los bordes para lograr un aspecto moderno y elegante en tus proyectos!
type: docs
weight: 110
url: /es/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

Obtiene o establece un valor que indica si el borde tiene sombra.

```csharp
public bool Shadow { get; set; }
```

## Observaciones

Obtiene el valor del primer borde de la colección.

Establece el valor para todos los bordes de la colección, excluidos los bordes diagonales.

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

* class [BorderCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
