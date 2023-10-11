---
title: Border.DistanceFromText
second_title: Référence de l'API Aspose.Words pour .NET
description: Border propriété. Obtient ou définit la distance de la bordure au texte ou au bord de la page en points.
type: docs
weight: 20
url: /fr/net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

Obtient ou définit la distance de la bordure au texte ou au bord de la page en points.

```csharp
public double DistanceFromText { get; set; }
```

### Remarques

N'a aucun effet et sera automatiquement remis à zéro pour les bordures des cellules du tableau.

### Exemples

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
* espace de noms [Aspose.Words](../../border/)
* Assemblée [Aspose.Words](../../../)


