---
title: Border.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words para .NET
description: ¡Descubre la propiedad Sombra de Borde para mejorar tu diseño! Controla los efectos de sombra para los bordes y realza tu interfaz de usuario con imágenes impactantes.
type: docs
weight: 60
url: /es/net/aspose.words/border/shadow/
---
## Border.Shadow property

Obtiene o establece un valor que indica si el borde tiene sombra.

```csharp
public bool Shadow { get; set; }
```

## Observaciones

En Microsoft Word, para que un borde tenga sombra, los bordes de los cuatro lados (izquierdo, superior, derecho e inferior) deben ser del mismo tipo, ancho y color, y todos deben tener la propiedad Sombra establecida en`verdadero`.

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

* class [Border](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
