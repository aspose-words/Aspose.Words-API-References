---
title: Margins Enum
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Margins pour personnaliser les marges de vos documents. Améliorez la mise en forme de vos documents grâce à des préréglages faciles à utiliser !
type: docs
weight: 4580
url: /fr/net/aspose.words/margins/
---
## Margins enumeration

Spécifie les marges prédéfinies.

```csharp
public enum Margins
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Normal | `0` | Marges normales. |
| Narrow | `1` | Marges étroites. |
| Moderate | `2` | Marges modérées. |
| Wide | `3` | Larges marges. |
| Mirrored | `4` | Marges en miroir. |
| Custom | `5` | Marges personnalisées. |

## Exemples

Indique quand recalculer la mise en page du document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// L'enregistrement d'un document au format PDF, dans une image ou l'impression pour la première fois sera automatiquement
// mettre en cache la mise en page du document dans ses pages.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modifier le document d'une manière ou d'une autre.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// Dans la version actuelle d'Aspose.Words, la modification du document ne le reconstruit pas automatiquement
// la mise en page en cache. Si nous souhaitons la mise en page en cache
// pour rester à jour, nous devrons le mettre à jour manuellement.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
