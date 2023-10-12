---
title: Border.Shadow
second_title: Référence de l'API Aspose.Words pour .NET
description: Border propriété. Obtient ou définit une valeur indiquant si la bordure a une ombre.
type: docs
weight: 60
url: /fr/net/aspose.words/border/shadow/
---
## Border.Shadow property

Obtient ou définit une valeur indiquant si la bordure a une ombre.

```csharp
public bool Shadow { get; set; }
```

### Remarques

Dans Microsoft Word, pour qu'une bordure ait une ombre, les bordures des quatre côtés (gauche, haut, droite et bas) doivent être du même type, largeur, couleur et toutes doivent avoir la propriété Shadow définie sur`vrai`.

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

* class [Border](../)
* espace de noms [Aspose.Words](../../border/)
* Assemblée [Aspose.Words](../../../)


