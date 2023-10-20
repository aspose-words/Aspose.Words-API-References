---
title: PageBorderDistanceFrom Enum
linktitle: PageBorderDistanceFrom
articleTitle: PageBorderDistanceFrom
second_title: Aspose.Words pour .NET
description: Aspose.Words.PageBorderDistanceFrom énumération. Spécifie le positionnement de la bordure de la page par rapport à la marge de la page en C#.
type: docs
weight: 4350
url: /fr/net/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enumeration

Spécifie le positionnement de la bordure de la page par rapport à la marge de la page.

```csharp
public enum PageBorderDistanceFrom
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Text | `0` | La position de la bordure est mesurée à partir de la marge de la page. |
| PageEdge | `1` | La position de la bordure est mesurée à partir du bord de la page. |

## Exemples

Montre comment créer une large bordure bleue en haut de la première page.

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

### Voir également

* class [PageSetup](../pagesetup/)
* property [BorderDistanceFrom](../pagesetup/borderdistancefrom/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
