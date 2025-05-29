---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
linktitle: ContinuousSectionPageNumberingRestart
articleTitle: ContinuousSectionPageNumberingRestart
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ContinuousSectionPageNumberingRestart de LayoutOptions pour un contrôle transparent de la numérotation des pages dans les sections continues. Optimisez la mise en page de votre document dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

Obtient ou définit le mode de comportement pour le calcul des numéros de page lorsqu'une section continue redémarre la numérotation des pages.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

## Remarques

La valeur par défaut estAlways . Cela correspond au comportement de MS Word 2019 qui était la dernière version au moment où l'option a été introduite. L'ancienne logique de numérotation des pages démontrée par MS Word 2016 est disponible via cette option. Veuillez[`ContinuousSectionRestart`](../../continuoussectionrestart/) pour la description du comportement.

## Exemples

Montre comment contrôler la numérotation des pages dans une section continue.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// Par défaut, le comportement d'Aspose.Words correspond à celui de Microsoft Word 2019.
// Si vous avez besoin de l'ancien comportement d'Aspose.Words, répétitif Microsoft Word 2016, utilisez « ContinuousSectionRestart.FromNewPageOnly ».
// La numérotation des pages redémarre uniquement s'il n'y a pas d'autre contenu avant la section sur la page où la section commence,
// à cause de cela, la numérotation sera réinitialisée à 2 à partir de la deuxième page.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Voir également

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* espace de noms [Aspose.Words.Layout](../../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../../)
