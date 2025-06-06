---
title: PdfImageCompression Enum
linktitle: PdfImageCompression
articleTitle: PdfImageCompression
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.PdfImageCompression pour optimiser la compression d'image dans vos fichiers PDF, améliorant la qualité et réduisant la taille du fichier sans effort.
type: docs
weight: 6280
url: /fr/net/aspose.words.saving/pdfimagecompression/
---
## PdfImageCompression enumeration

Spécifie le type de compression appliqué aux images dans le fichier PDF.

```csharp
public enum PdfImageCompression
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Auto | `0` | Sélectionne automatiquement la compression la plus appropriée pour chaque image. |
| Jpeg | `1` | Compression Jpeg. Ne prend pas en charge la transparence. |

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
