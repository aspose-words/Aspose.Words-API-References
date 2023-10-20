---
title: BorderCollection.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words pour .NET
description: BorderCollection Color propriété. Obtient ou définit la couleur de la bordure en C#.
type: docs
weight: 20
url: /fr/net/aspose.words/bordercollection/color/
---
## BorderCollection.Color property

Obtient ou définit la couleur de la bordure.

```csharp
public Color Color { get; set; }
```

## Remarques

Renvoie la couleur de la première bordure de la collection.

Définit la couleur de toutes les bordures de la collection, à l'exception des bordures diagonales.

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
