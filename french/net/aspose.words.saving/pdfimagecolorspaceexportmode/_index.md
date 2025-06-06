---
title: PdfImageColorSpaceExportMode Enum
linktitle: PdfImageColorSpaceExportMode
articleTitle: PdfImageColorSpaceExportMode
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words PdfImageColorSpaceExportMode pour optimiser la sélection des couleurs d'image dans vos documents PDF pour des visuels époustouflants.
type: docs
weight: 6270
url: /fr/net/aspose.words.saving/pdfimagecolorspaceexportmode/
---
## PdfImageColorSpaceExportMode enumeration

Spécifie comment l'espace colorimétrique sera sélectionné pour les images dans le document PDF.

```csharp
public enum PdfImageColorSpaceExportMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Auto | `0` | Aspose.Words sélectionne automatiquement l'espace colorimétrique le plus approprié pour chaque image. |
| SimpleCmyk | `1` | Aspose.Words convertit les images RVB en espace colorimétrique CMJN à l'aide d'une formule simple. |

## Exemples

Montre comment définir un espace colorimétrique différent pour les images d'un document lorsque nous l'exportons au format PDF.

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

// Définissez la propriété « ImageColorSpaceExportMode » sur « PdfImageColorSpaceExportMode.Auto » pour obtenir Aspose.Words
// sélectionne automatiquement l'espace colorimétrique des images dans le document qu'il convertit en PDF.
// Dans la plupart des cas, l'espace colorimétrique sera RVB.
// Définissez la propriété « ImageColorSpaceExportMode » sur « PdfImageColorSpaceExportMode.SimpleCmyk »
// pour utiliser l'espace colorimétrique CMJN pour toutes les images du PDF enregistré.
// Aspose.Words appliquera également la compression Flate à toutes les images et ignorera la valeur de la propriété « ImageCompression ».
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
