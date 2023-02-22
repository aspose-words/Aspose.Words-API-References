---
title: PdfSaveOptions.PreblendImages
second_title: Référence de l'API Aspose.Words pour .NET
description: PdfSaveOptions propriété. Obtient ou définit une valeur déterminant sil faut ou non prémélanger les images transparentes avec une couleur darrièreplan noire.
type: docs
weight: 230
url: /fr/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Obtient ou définit une valeur déterminant s'il faut ou non pré-mélanger les images transparentes avec une couleur d'arrière-plan noire.

```csharp
public bool PreblendImages { get; set; }
```

### Remarques

Le prémélange d'images peut améliorer l'apparence visuelle du document PDF dans Adobe Reader et supprimer les artefacts d'anticrénelage.

Afin d'afficher correctement les images prémélangées, l'application de visionneuse PDF doit prendre en charge l'entrée /Matte dans le dictionnaire d'images de masque souple. De plus, le prémélange des images peut réduire les performances de rendu PDF.

La valeur par défaut est`faux`.

### Exemples

Montre comment pré-mélanger des images avec des arrière-plans transparents lors de l'enregistrement d'un document au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "PreblendImages" sur "true" pour préfusionner les images transparentes
// avec un arrière-plan, ce qui peut réduire les artefacts.
// Définissez la propriété "PreblendImages" sur "false" pour rendre les images transparentes normalement.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

Montre comment pré-mélanger des images avec des arrière-plans transparents (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "PreblendImages" sur "true" pour préfusionner les images transparentes
// avec un arrière-plan, ce qui peut réduire les artefacts.
// Définissez la propriété "PreblendImages" sur "false" pour rendre les images transparentes normalement.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImagesNetStandard2.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../pdfsaveoptions/)
* Assemblée [Aspose.Words](../../../)


