---
title: ColorMode Enum
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Saving.ColorMode pour un rendu des couleurs optimisé. Améliorez l'attrait visuel de votre document grâce à des paramètres de couleur précis.
type: docs
weight: 5600
url: /fr/net/aspose.words.saving/colormode/
---
## ColorMode enumeration

Spécifie comment les couleurs sont rendues.

```csharp
public enum ColorMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Normal | `0` | Rendu avec des couleurs non modifiées. |
| Grayscale | `1` | Rendu avec des couleurs dans une gamme de nuances de gris allant du blanc au noir. |

## Exemples

Montre comment modifier la couleur de l'image avec la propriété des options d'enregistrement.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
// Définissez la propriété « ColorMode » sur « Niveaux de gris » pour rendre toutes les images du document en noir et blanc.
// La taille du document de sortie peut être plus grande avec ce paramètre.
// Définissez la propriété « ColorMode » sur « Normal » pour restituer toutes les images en couleur.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
