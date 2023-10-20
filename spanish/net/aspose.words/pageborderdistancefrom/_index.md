---
title: PageBorderDistanceFrom Enum
linktitle: PageBorderDistanceFrom
articleTitle: PageBorderDistanceFrom
second_title: Aspose.Words para .NET
description: Aspose.Words.PageBorderDistanceFrom enumeración. Especifica la posición del borde de la página en relación con el margen de la página en C#.
type: docs
weight: 4350
url: /es/net/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enumeration

Especifica la posición del borde de la página en relación con el margen de la página.

```csharp
public enum PageBorderDistanceFrom
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Text | `0` | La posición del borde se mide desde el margen de la página. |
| PageEdge | `1` | La posición del borde se mide desde el borde de la página. |

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

* class [PageSetup](../pagesetup/)
* property [BorderDistanceFrom](../pagesetup/borderdistancefrom/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
