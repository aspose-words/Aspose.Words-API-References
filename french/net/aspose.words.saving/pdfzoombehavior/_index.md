---
title: Enum PdfZoomBehavior
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.PdfZoomBehavior énumération. Spécifie le type de zoom appliqué à un document PDF lorsquil est ouvert dans une visionneuse PDF.
type: docs
weight: 5260
url: /fr/net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

Spécifie le type de zoom appliqué à un document PDF lorsqu'il est ouvert dans une visionneuse PDF.

```csharp
public enum PdfZoomBehavior
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | La façon dont le document est affiché est laissée à la visionneuse PDF. Habituellement, le visualiseur affiche le document pour s'adapter à la largeur de la page. |
| ZoomFactor | `1` | Affiche la page en utilisant le facteur de zoom spécifié. |
| FitPage | `2` | Affiche la page afin qu'elle soit entièrement visible. |
| FitWidth | `3` | S'adapte à la largeur de la page. |
| FitHeight | `4` | S'adapte à la hauteur de la page. |
| FitBox | `5` | S'adapte à la boîte englobante (rectangle contenant tous les éléments visibles sur la page). |

### Exemples

Montre comment définir le zoom par défaut qu'un lecteur applique lors de l'ouverture d'un document PDF rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
// Définissez la propriété "ZoomBehavior" sur "PdfZoomBehavior.ZoomFactor" pour obtenir un lecteur PDF
// applique un facteur de zoom basé sur un pourcentage lorsque nous ouvrons le document avec.
// Définissez la propriété "ZoomFactor" sur "25" pour donner au facteur de zoom une valeur de 25 %.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// Lorsque nous ouvrons ce document à l'aide d'un lecteur tel qu'Adobe Acrobat, nous verrons le document mis à l'échelle à 1/4 de sa taille réelle.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


