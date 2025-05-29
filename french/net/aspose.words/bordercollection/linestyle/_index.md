---
title: BorderCollection.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words pour .NET
description: Découvrez la propriété BorderCollection LineStyle pour personnaliser votre design avec des styles de bordure flexibles. Améliorez l'esthétique de votre projet sans effort !
type: docs
weight: 80
url: /fr/net/aspose.words/bordercollection/linestyle/
---
## BorderCollection.LineStyle property

Obtient ou définit le style de bordure.

```csharp
public LineStyle LineStyle { get; set; }
```

## Remarques

Renvoie le style de la première bordure de la collection.

Définit le style de toutes les bordures de la collection, à l'exclusion des bordures diagonales.

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

* enum [LineStyle](../../linestyle/)
* class [BorderCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
