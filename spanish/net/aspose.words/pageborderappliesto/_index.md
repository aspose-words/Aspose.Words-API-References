---
title: PageBorderAppliesTo Enum
linktitle: PageBorderAppliesTo
articleTitle: PageBorderAppliesTo
second_title: Aspose.Words para .NET
description: Aspose.Words.PageBorderAppliesTo enumeración. Especifica en qué páginas se imprime el borde de la página en C#.
type: docs
weight: 4340
url: /es/net/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enumeration

Especifica en qué páginas se imprime el borde de la página.

```csharp
public enum PageBorderAppliesTo
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| AllPages | `0` | El borde de la página se muestra en todas las páginas de la sección. |
| FirstPage | `1` | El borde de la página se muestra solo en la primera página de la sección. |
| OtherPages | `2` | El borde de la página se muestra en todas las páginas excepto en la primera página de la sección. |

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
* property [BorderAppliesTo](../pagesetup/borderappliesto/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
