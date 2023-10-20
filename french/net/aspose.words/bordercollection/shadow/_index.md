---
title: BorderCollection.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words pour .NET
description: BorderCollection Shadow propriété. Obtient ou définit une valeur indiquant si la bordure a une ombre en C#.
type: docs
weight: 110
url: /fr/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

Obtient ou définit une valeur indiquant si la bordure a une ombre.

```csharp
public bool Shadow { get; set; }
```

## Remarques

Obtient la valeur de la première bordure de la collection.

Définit la valeur de toutes les bordures de la collection, à l'exception des bordures diagonales.

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
