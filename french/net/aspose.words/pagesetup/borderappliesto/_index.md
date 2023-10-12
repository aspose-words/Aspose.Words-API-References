---
title: PageSetup.BorderAppliesTo
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSetup propriété. Spécifie sur quelles pages la bordure de page est imprimée.
type: docs
weight: 30
url: /fr/net/aspose.words/pagesetup/borderappliesto/
---
## PageSetup.BorderAppliesTo property

Spécifie sur quelles pages la bordure de page est imprimée.

```csharp
public PageBorderAppliesTo BorderAppliesTo { get; set; }
```

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

* enum [PageBorderAppliesTo](../../pageborderappliesto/)
* class [PageSetup](../)
* espace de noms [Aspose.Words](../../pagesetup/)
* Assemblée [Aspose.Words](../../../)


