---
title: PdfSaveOptions.PreblendImages
linktitle: PreblendImages
articleTitle: PreblendImages
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PreblendImages de PdfSaveOptions. Contrôlez facilement la fusion des images transparentes pour une qualité de document et un attrait visuel améliorés.
type: docs
weight: 270
url: /fr/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Obtient ou définit une valeur déterminant s'il faut ou non pré-mélanger les images transparentes avec une couleur d'arrière-plan noire.

```csharp
public bool PreblendImages { get; set; }
```

## Remarques

Le prémélange d'images peut améliorer l'apparence visuelle du document PDF dans Adobe Reader et supprimer les artefacts d'anticrénelage.

Afin d'afficher correctement les images pré-mélangées, l'application de visualisation PDF doit prendre en charge l'entrée /Matte dans le dictionnaire d'images à masque souple. De plus, le pré-mélange d'images peut diminuer les performances de rendu PDF.

La valeur par défaut est`FAUX`.

## Exemples

Montre comment pré-mélanger des images avec des arrière-plans transparents lors de l'enregistrement d'un document au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Définissez la propriété « PreblendImages » sur « true » pour pré-mélanger les images transparentes
// avec un arrière-plan, ce qui peut réduire les artefacts.
// Définissez la propriété « PreblendImages » sur « false » pour restituer les images transparentes normalement.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
