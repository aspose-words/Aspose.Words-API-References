---
title: ContinuousSectionRestart Enum
linktitle: ContinuousSectionRestart
articleTitle: ContinuousSectionRestart
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Layout.ContinuousSectionRestart pour des options de numérotation flexibles dans les sections continues. Améliorez la mise en page de vos documents sans effort !
type: docs
weight: 3750
url: /fr/net/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enumeration

Représente différents comportements lors du calcul des numéros de page dans une section continue qui redémarre la numérotation des pages.

```csharp
public enum ContinuousSectionRestart
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Always | `0` | La numérotation des pages redémarre toujours quel que soit le flux de contenu. |
| FromNewPageOnly | `1` | La numérotation des pages redémarre uniquement s'il n'y a pas d'autre contenu avant la section sur la page où la section commence. |

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

* espace de noms [Aspose.Words.Layout](../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../)
