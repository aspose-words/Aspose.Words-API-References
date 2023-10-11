---
title: PdfSaveOptions.InterpolateImages
second_title: Référence de l'API Aspose.Words pour .NET
description: PdfSaveOptions propriété. Un indicateur indiquant si linterpolation dimage doit être effectuée par un lecteur conforme. LorsqueFAUX est spécifié lindicateur nest pas écrit dans le document de sortie et le comportement par défaut du lecteur est utilisé à la place.
type: docs
weight: 210
url: /fr/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

Un indicateur indiquant si l'interpolation d'image doit être effectuée par un lecteur conforme. Lorsque`FAUX` est spécifié, l'indicateur n'est pas écrit dans le document de sortie et le comportement par défaut du lecteur est utilisé à la place.

```csharp
public bool InterpolateImages { get; set; }
```

### Remarques

Lorsque la résolution d'une image source est nettement inférieure à celle du périphérique de sortie, chaque échantillon source couvre de nombreux pixels du périphérique. En conséquence, les images peuvent apparaître irrégulières ou en blocs. Ces artefacts visuels peuvent être réduits en appliquant un algorithme d'interpolation d'image pendant le rendu. Au lieu de peindre tous les pixels couverts par un échantillon source avec la même couleur, l'interpolation d'image tente de produire un rendu fluide. transition entre des valeurs d'échantillon adjacentes.

Un lecteur conforme peut choisir de ne pas implémenter cette fonctionnalité de PDF, ou peut utiliser toute implémentation spécifique d'interpolation qu'il souhaite.

La valeur par défaut est`FAUX`.

L’indicateur d’interpolation est interdit par la conformité PDF/A.`FAUX` La valeur sera utilisée automatiquement lors de l'enregistrement au format PDF/A.

### Exemples

Montre comment effectuer une interpolation sur des images lors de l'enregistrement d'un document au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Définissez la propriété "InterpolateImages" sur "true" pour que le lecteur qui ouvre ce document interpole les images.
// Leur résolution doit être inférieure à celle de l'appareil qui affiche le document.
// Définissez la propriété "InterpolateImages" sur "false" pour que le lecteur n'applique aucune interpolation.
saveOptions.InterpolateImages = interpolateImages;

// Lorsque nous ouvrirons ce document avec un lecteur tel qu'Adobe Acrobat, nous devrons zoomer sur l'image
// pour voir l'effet d'interpolation si nous avons enregistré le document avec cette option activée.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

Montre comment améliorer la qualité d'une image dans les documents rendus (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Définissez la propriété "InterpolateImages" sur "true" pour que le lecteur qui ouvre ce document interpole les images.
// Leur résolution doit être inférieure à celle de l'appareil qui affiche le document.
// Définissez la propriété "InterpolateImages" sur "false" pour que le lecteur n'applique aucune interpolation.
saveOptions.InterpolateImages = interpolateImages;

// Lorsque nous ouvrirons ce document avec un lecteur tel qu'Adobe Acrobat, nous devrons zoomer sur l'image
// pour voir l'effet d'interpolation si nous avons enregistré le document avec cette option activée.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImagesNetStandard2.pdf", saveOptions);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../pdfsaveoptions/)
* Assemblée [Aspose.Words](../../../)


