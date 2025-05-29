---
title: PdfSaveOptions.InterpolateImages
linktitle: InterpolateImages
articleTitle: InterpolateImages
second_title: Aspose.Words pour .NET
description: Découvrez la propriété InterpolateImages de PdfSaveOptions, une fonctionnalité clé qui améliore la qualité d'image de vos documents. Optimisez vos PDF sans effort !
type: docs
weight: 210
url: /fr/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

Un indicateur indiquant si l'interpolation d'image doit être effectuée par un lecteur conforme. Lorsque`FAUX` est spécifié, l'indicateur n'est pas écrit dans le document de sortie et le comportement par défaut du lecteur est utilisé à la place.

```csharp
public bool InterpolateImages { get; set; }
```

## Remarques

Lorsque la résolution d'une image source est nettement inférieure à celle du périphérique de sortie, chaque échantillon source couvre de nombreux pixels. Par conséquent, les images peuvent apparaître irrégulières ou irrégulières. Ces artefacts visuels peuvent être réduits en appliquant un algorithme d'interpolation d'image lors du rendu. Au lieu de peindre tous les pixels couverts par un échantillon source avec la même couleur, l'interpolation d'image tente de produire une transition fluide entre les valeurs d'échantillons adjacentes.

Un lecteur conforme peut choisir de ne pas implémenter cette fonctionnalité du PDF, ou peut utiliser toute implémentation spécifique d'interpolation qu'il souhaite.

La valeur par défaut est`FAUX`.

L'indicateur d'interpolation est interdit par la conformité PDF/A.`FAUX` la valeur sera utilisée automatiquement lors de l'enregistrement au format PDF/A.

## Exemples

Montre comment effectuer une interpolation sur des images lors de l'enregistrement d'un document au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Définissez la propriété « InterpolateImages » sur « true » pour que le lecteur qui ouvre ce document interpole les images.
// Leur résolution doit être inférieure à celle de l'appareil qui affiche le document.
// Définissez la propriété « InterpolateImages » sur « false » pour que le lecteur n'applique aucune interpolation.
saveOptions.InterpolateImages = interpolateImages;

// Lorsque nous ouvrons ce document avec un lecteur tel qu'Adobe Acrobat, nous devrons zoomer sur l'image
// pour voir l'effet d'interpolation si nous avons enregistré le document avec celui-ci activé.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
