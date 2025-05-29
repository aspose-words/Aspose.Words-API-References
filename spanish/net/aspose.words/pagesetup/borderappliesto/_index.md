---
title: PageSetup.BorderAppliesTo
linktitle: BorderAppliesTo
articleTitle: BorderAppliesTo
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad PageSetup BorderAppliesTo mejora el diseño de su documento al controlar la impresión del borde de página para lograr una apariencia pulida y profesional.
type: docs
weight: 30
url: /es/net/aspose.words/pagesetup/borderappliesto/
---
## PageSetup.BorderAppliesTo property

Especifica en qué páginas se imprime el borde de la página.

```csharp
public PageBorderAppliesTo BorderAppliesTo { get; set; }
```

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

* enum [PageBorderAppliesTo](../../pageborderappliesto/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
