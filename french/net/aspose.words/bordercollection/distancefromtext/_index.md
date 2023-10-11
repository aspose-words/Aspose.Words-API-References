---
title: BorderCollection.DistanceFromText
second_title: Référence de l'API Aspose.Words pour .NET
description: BorderCollection propriété. Obtient ou définit la distance entre la bordure et le texte en points.
type: docs
weight: 40
url: /fr/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

Obtient ou définit la distance entre la bordure et le texte en points.

```csharp
public double DistanceFromText { get; set; }
```

### Remarques

Obtient la distance du texte pour la première bordure.

Définit la distance par rapport au texte pour toutes les bordures de la collection, à l'exception des bordures diagonales.

N'a aucun effet et sera automatiquement réinitialisé à zéro pour les bordures des cellules du tableau.

### Exemples

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
* espace de noms [Aspose.Words](../../bordercollection/)
* Assemblée [Aspose.Words](../../../)


