---
title: Border.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words para .NET
description: Border DistanceFromText propiedad. Obtiene o establece la distancia del borde desde el texto o desde el borde de la página en puntos en C#.
type: docs
weight: 20
url: /es/net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

Obtiene o establece la distancia del borde desde el texto o desde el borde de la página en puntos.

```csharp
public double DistanceFromText { get; set; }
```

## Observaciones

No tiene ningún efecto y se restablecerá automáticamente a cero para los bordes de las celdas de la tabla.

## Ejemplos

Muestra cómo crear un borde de banda azul ancho en la parte superior de la primera página.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
```

### Ver también

* class [Border](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
