---
title: PdfSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words pour .NET
description: Optimisez vos images PDF avec la propriété JpegQuality de PdfSaveOptions, vous permettant de contrôler la qualité JPEG pour des visuels de documents époustouflants.
type: docs
weight: 220
url: /fr/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

Obtient ou définit une valeur déterminant la qualité des images JPEG dans le document PDF.

```csharp
public int JpegQuality { get; set; }
```

## Remarques

La valeur par défaut est 100.

Cette propriété est utilisée en conjonction avec le[`ImageCompression`](../imagecompression/) option.

N'a d'effet que lorsqu'un document contient des images JPEG.

Utilisez cette propriété pour obtenir ou définir la qualité des images à l'intérieur d'un document lors de l'enregistrement au format PDF. La valeur peut varier de 0 à 100 où 0 signifie la pire qualité mais la compression maximale et 100 signifie la meilleure qualité mais la compression minimale. Si la qualité est de 100 et que l'image source est JPEG, cela signifie qu'il n'y a pas de compression - les octets d'origine seront enregistrés.

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

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
