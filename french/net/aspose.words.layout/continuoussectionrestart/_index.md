---
title: Enum ContinuousSectionRestart
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Layout.ContinuousSectionRestart énumération. Représente différents comportements lors du calcul des numéros de page dans une section continue qui redémarre la numérotation des pages.
type: docs
weight: 3300
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
| FromNewPageOnly | `1` | La numérotation des pages redémarre uniquement s'il n'y a aucun autre contenu avant la section sur la page où commence la section. |

### Exemples

Montre comment contrôler la numérotation des pages dans une section continue.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// Par défaut, le comportement d'Aspose.Words correspond à celui de Microsoft Word 2019.
// Si vous avez besoin de l'ancien comportement Aspose.Words, répétitif de Microsoft Word 2016, utilisez 'ContinuousSectionRestart.FromNewPageOnly'.
// La numérotation des pages redémarre uniquement s'il n'y a aucun autre contenu avant la section sur la page où commence la section,
// de ce fait la numérotation sera réinitialisée à 2 à partir de la deuxième page.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Voir également

* espace de noms [Aspose.Words.Layout](../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../)


