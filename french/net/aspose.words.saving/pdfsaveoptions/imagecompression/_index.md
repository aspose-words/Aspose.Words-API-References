---
title: PdfSaveOptions.ImageCompression
linktitle: ImageCompression
articleTitle: ImageCompression
second_title: Aspose.Words pour .NET
description: Optimisez votre PDF avec la propriété ImageCompression de PdfSaveOptions, vous permettant de choisir le meilleur type de compression pour des images dynamiques et de haute qualité.
type: docs
weight: 200
url: /fr/net/aspose.words.saving/pdfsaveoptions/imagecompression/
---
## PdfSaveOptions.ImageCompression property

Spécifie le type de compression à utiliser pour toutes les images du document.

```csharp
public PdfImageCompression ImageCompression { get; set; }
```

## Remarques

La valeur par défaut estAuto.

En utilisantJpeg vous permet de contrôler la qualité des images dans le document de sortie via le[`JpegQuality`](../jpegquality/) propriété.

En utilisantJpeg offre la vitesse de conversion la plus rapide par rapport aux performances des autres types de compression, mais dans ce cas, il y a une compression JPEG avec perte.

En utilisantAuto permet de contrôler la qualité du Jpeg dans le document de sortie via le[`JpegQuality`](../jpegquality/)propriété, mais pour d'autres formats, les données de pixels brutes sont extraites et enregistrées avec la compression Flate. Ce cas est plus lent que la conversion Jpeg mais sans perte.

## Exemples

Montre comment spécifier un type de compression pour toutes les images d'un document que nous convertissons en PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
// Définissez la propriété « ImageCompression » sur « PdfImageCompression.Auto » pour utiliser le
// Propriété "ImageCompression" pour contrôler la qualité des images Jpeg qui finissent dans le PDF de sortie.
// Définissez la propriété « ImageCompression » sur « PdfImageCompression.Jpeg » pour utiliser le
// Propriété « ImageCompression » pour contrôler la qualité de toutes les images qui se retrouvent dans le PDF de sortie.
pdfSaveOptions.ImageCompression = pdfImageCompression;
// Définissez la propriété « JpegQuality » sur « 10 » pour renforcer la compression au détriment de la qualité de l'image.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Voir également

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
