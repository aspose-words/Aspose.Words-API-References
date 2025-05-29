---
title: ImageSaveOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words pour .NET
description: Optimisez vos images avec ImageSaveOptions ! Contrôlez la résolution horizontale et verticale en DPI pour une qualité et une clarté exceptionnelles. Améliorez vos visuels dès aujourd'hui !
type: docs
weight: 130
url: /fr/net/aspose.words.saving/imagesaveoptions/resolution/
---
## ImageSaveOptions.Resolution property

Définit la résolution horizontale et verticale des images générées, en points par pouce.

```csharp
public float Resolution { set; }
```

## Remarques

Cette propriété n'a d'effet que lors de l'enregistrement dans des formats d'image raster.

## Exemples

Montre comment spécifier une résolution lors du rendu d'un document au format PNG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Créez un objet « ImageSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode rend le document en image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

// Définissez la propriété « Résolution » sur « 72 » pour rendre le document en 72 dpi.
options.Resolution = 72;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

// Définissez la propriété « Résolution » sur « 300 » pour rendre le document en 300 dpi.
options.Resolution = 300;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);
```

### Voir également

* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
