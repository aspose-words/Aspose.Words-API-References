---
title: BorderCollection.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words pour .NET
description: Découvrez la propriété BorderCollection LineWidth pour ajuster facilement la largeur de la bordure en points, améliorant ainsi la précision et l'attrait visuel de votre conception.
type: docs
weight: 90
url: /fr/net/aspose.words/bordercollection/linewidth/
---
## BorderCollection.LineWidth property

Obtient ou définit la largeur de la bordure en points.

```csharp
public double LineWidth { get; set; }
```

## Remarques

Renvoie la largeur de la première bordure de la collection.

Définit la largeur de toutes les bordures de la collection, à l'exclusion des bordures diagonales.

## Exemples

Montre comment créer une bordure de page ondulée verte avec une ombre.

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

### Voir également

* class [BorderCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
