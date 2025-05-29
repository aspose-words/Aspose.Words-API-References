---
title: PageBorderAppliesTo Enum
linktitle: PageBorderAppliesTo
articleTitle: PageBorderAppliesTo
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.PageBorderAppliesTo pour contrôler l'impression des bordures de page sur des pages spécifiques pour une mise en forme améliorée des documents.
type: docs
weight: 5070
url: /fr/net/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enumeration

Spécifie sur quelles pages la bordure de page est imprimée.

```csharp
public enum PageBorderAppliesTo
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| AllPages | `0` | La bordure de page est affichée sur toutes les pages de la section. |
| FirstPage | `1` | La bordure de page est affichée uniquement sur la première page de la section. |
| OtherPages | `2` | La bordure de page est affichée sur toutes les pages sauf la première page de la section. |

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

* class [PageSetup](../pagesetup/)
* property [BorderAppliesTo](../pagesetup/borderappliesto/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
