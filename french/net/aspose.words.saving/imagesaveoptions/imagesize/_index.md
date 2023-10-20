---
title: ImageSaveOptions.ImageSize
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words pour .NET
description: ImageSaveOptions ImageSize propriété. Obtient ou définit la taille dune image générée en pixels en C#.
type: docs
weight: 70
url: /fr/net/aspose.words.saving/imagesaveoptions/imagesize/
---
## ImageSaveOptions.ImageSize property

Obtient ou définit la taille d'une image générée en pixels.

```csharp
public Size ImageSize { get; set; }
```

## Remarques

Cette propriété n'a d'effet que lors de l'enregistrement au format d'image raster.

La valeur par défaut est (0 x 0), ce qui signifie que la taille de l'image générée sera calculée en fonction de la taille de l'image en points, de la résolution et de l'échelle spécifiées.

## Exemples

Montre comment restituer chaque page d’un document dans une image TIFF distincte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Crée un objet "ImageSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la manière dont cette méthode restitue le document en image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Fixe la propriété "PageSet" au numéro de la première page de
    // à partir duquel commencer le rendu du document.
    options.PageSet = new PageSet(i);
    // Exporter la page à 2325x5325 pixels et 600 dpi.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

### Voir également

* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
