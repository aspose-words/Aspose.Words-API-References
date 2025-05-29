---
title: ImageSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words pour .NET
description: Découvrez la méthode ImageSaveOptions Clone pour créer sans effort un clone profond de vos objets, améliorant ainsi votre efficacité et votre flexibilité de codage.
type: docs
weight: 210
url: /fr/net/aspose.words.saving/imagesaveoptions/clone/
---
## ImageSaveOptions.Clone method

Crée un clone profond de cet objet.

```csharp
public ImageSaveOptions Clone()
```

## Exemples

Montre comment sélectionner un débit de bits par pixel avec lequel restituer un document en image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Lorsque nous enregistrons le document sous forme d'image, nous pouvons passer un objet SaveOptions à
// sélectionnez un format de pixel pour l'image que l'opération de sauvegarde générera.
// Différents débits de bits par pixel affecteront la qualité et la taille du fichier de l'image générée.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// Nous pouvons cloner des instances ImageSaveOptions.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Voir également

* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
