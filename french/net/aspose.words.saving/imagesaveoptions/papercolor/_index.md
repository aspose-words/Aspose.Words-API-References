---
title: ImageSaveOptions.PaperColor
linktitle: PaperColor
articleTitle: PaperColor
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PaperColor ImageSaveOptions pour personnaliser facilement les couleurs d'arrière-plan de vos images générées, améliorant ainsi l'attrait visuel et l'unicité.
type: docs
weight: 110
url: /fr/net/aspose.words.saving/imagesaveoptions/papercolor/
---
## ImageSaveOptions.PaperColor property

Obtient ou définit la couleur d'arrière-plan (papier) pour les images générées.

La valeur par défaut estWhite.

```csharp
public Color PaperColor { get; set; }
```

## Remarques

Lors du rendu des pages d'un document qui spécifie sa propre couleur d'arrière-plan, , la couleur d'arrière-plan du document remplacera la couleur spécifiée par cette propriété.

## Exemples

Rend une page d'un document Word dans une image avec un arrière-plan transparent ou coloré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Créez un objet « ImageSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode rend le document en image.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);
// Définissez la propriété « PaperColor » sur une couleur transparente pour appliquer une transparence
// arrière-plan du document lors de son rendu en image.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Définissez la propriété « PaperColor » sur une couleur opaque pour appliquer cette couleur
// comme arrière-plan du document lorsque nous le rendons sous forme d'image.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### Voir également

* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
