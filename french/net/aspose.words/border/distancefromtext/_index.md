---
title: Border.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Border DistanceFromText pour ajuster facilement l'espacement des bordures à partir du texte ou des bords de page en points pour un contrôle de mise en page amélioré.
type: docs
weight: 20
url: /fr/net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

Obtient ou définit la distance de la bordure par rapport au texte ou au bord de la page en points.

```csharp
public double DistanceFromText { get; set; }
```

## Remarques

N'a aucun effet et sera automatiquement réinitialisé à zéro pour les bordures des cellules du tableau.

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

* class [Border](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
