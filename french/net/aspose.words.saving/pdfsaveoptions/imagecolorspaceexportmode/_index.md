---
title: PdfSaveOptions.ImageColorSpaceExportMode
linktitle: ImageColorSpaceExportMode
articleTitle: ImageColorSpaceExportMode
second_title: Aspose.Words pour .NET
description: PdfSaveOptions ImageColorSpaceExportMode propriété. Spécifie comment lespace colorimétrique sera sélectionné pour les images dans le document PDF en C#.
type: docs
weight: 190
url: /fr/net/aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/
---
## PdfSaveOptions.ImageColorSpaceExportMode property

Spécifie comment l'espace colorimétrique sera sélectionné pour les images dans le document PDF.

```csharp
public PdfImageColorSpaceExportMode ImageColorSpaceExportMode { get; set; }
```

## Remarques

La valeur par défaut estAuto .

SiSimpleCmyk la valeur est spécifiée, [`ImageCompression`](../imagecompression/) L'option est ignorée et La compression Flate est utilisée pour toutes les images du document.

SimpleCmyk la valeur n'est pas prise en charge lors de l'enregistrement au format PDF/A. Auto la valeur sera utilisée à la place.

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

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Définissez la propriété "ImageColorSpaceExportMode" sur "PdfImageColorSpaceExportMode.Auto" pour obtenir Aspose.Words
// sélectionne automatiquement l'espace colorimétrique des images du document qu'il convertit en PDF.
// Dans la plupart des cas, l'espace colorimétrique sera RVB.
// Définit la propriété "ImageColorSpaceExportMode" sur "PdfImageColorSpaceExportMode.SimpleCmyk"
// pour utiliser l'espace colorimétrique CMJN pour toutes les images du PDF enregistré.
// Aspose.Words appliquera également la compression Flate à toutes les images et ignorera la valeur de la propriété "ImageCompression".
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### Voir également

* enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
