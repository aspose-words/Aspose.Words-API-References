---
title: MarkdownSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ImagesFolderAlias de MarkdownSaveOptions pour gérer facilement les URI des images dans vos documents. Simplifiez votre flux de travail grâce à cette fonctionnalité essentielle !
type: docs
weight: 90
url: /fr/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Spécifie le nom du dossier utilisé pour construire les URI d'image écrites dans un document. La valeur par défaut est une chaîne vide.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Remarques

Lorsque vous enregistrez un[`Document`](../../../aspose.words/document/) dansMarkdown format, Aspose.Words doit enregistrer toutes les images intégrées dans le document sous forme de fichiers autonomes. [`ImagesFolder`](../imagesfolder/) vous permet de spécifier où les images seront enregistrées et `ImagesFolderAlias` permet de spécifier comment les URI des images seront construits.

Si`ImagesFolderAlias` n'est pas une chaîne vide, alors l'URI de l'image written vers Markdown seraImagesFolderAlias + &lt;nom du fichier image&gt;.

Si`ImagesFolderAlias` est une chaîne vide, alors l'URI de l'image written vers Markdown seraImagesFolder + &lt;nom du fichier image&gt;.

Si`ImagesFolderAlias` est défini sur '.' (point), alors le nom du fichier image sera écrit dans Markdown sans chemin, quelles que soient les autres options.

## Exemples

Montre comment spécifier le nom du dossier utilisé pour construire les URI d'image.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
builder.InsertImage(ImageDir + "Logo.jpg");

string imagesFolder = Path.Combine(ArtifactsDir, "ImagesDir");
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Utilisez la propriété « ImagesFolder » pour attribuer un dossier dans le système de fichiers local dans lequel
// Aspose.Words enregistrera toutes les images liées du document.
saveOptions.ImagesFolder = imagesFolder;
// Utilisez la propriété « ImagesFolderAlias » pour utiliser ce dossier
// lors de la construction d'URI d'image au lieu du nom du dossier d'images.
saveOptions.ImagesFolderAlias = "http://exemple.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### Voir également

* class [MarkdownSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
