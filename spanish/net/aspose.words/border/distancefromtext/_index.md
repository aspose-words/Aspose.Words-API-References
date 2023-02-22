---
title: Border.DistanceFromText
second_title: Referencia de API de Aspose.Words para .NET
description: Border propiedad. Obtiene o establece la distancia del borde al texto o al borde de la página en puntos.
type: docs
weight: 20
url: /es/net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

Obtiene o establece la distancia del borde al texto o al borde de la página en puntos.

```csharp
public double DistanceFromText { get; set; }
```

### Observaciones

No tiene efecto y se restablecerá automáticamente a cero para los bordes de las celdas de la tabla.

### Ejemplos

Muestra cómo crear un borde ancho de banda azul en la parte superior de la primera página.

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
* espacio de nombres [Aspose.Words](../../border/)
* asamblea [Aspose.Words](../../../)


