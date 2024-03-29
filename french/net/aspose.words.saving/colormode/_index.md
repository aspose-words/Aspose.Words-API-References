---
title: ColorMode Enum
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words pour .NET
description: Aspose.Words.Saving.ColorMode énumération. Spécifie comment les couleurs sont rendues en C#.
type: docs
weight: 4860
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

Montre comment changer la couleur de l’image avec la propriété des options d’enregistrement.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
// Définissez la propriété "ColorMode" sur "Grayscale" pour restituer toutes les images du document en noir et blanc.
// La taille du document de sortie peut être plus grande avec ce paramètre.
// Définissez la propriété "ColorMode" sur "Normal" pour restituer toutes les images en couleur.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
