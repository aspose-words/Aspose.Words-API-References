---
title: MarkdownSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ImagesFolder de MarkdownSaveOptions améliore vos exportations de documents en spécifiant le dossier idéal pour enregistrer les images au format Markdown.
type: docs
weight: 80
url: /fr/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Spécifie le dossier physique dans lequel les images sont enregistrées lors de l'exportation d'un document vers leMarkdown format. La valeur par défaut est une chaîne vide.

```csharp
public string ImagesFolder { get; set; }
```

## Remarques

Lorsque vous enregistrez un[`Document`](../../../aspose.words/document/) dansMarkdownformat, Aspose.Words doit enregistrer toutes les images intégrées dans le document sous forme de fichiers autonomes. `ImagesFolder` vous permet de spécifier où les images seront enregistrées.

Si vous enregistrez un document dans un fichier et fournissez un nom de fichier, Aspose.Words, par défaut, enregistre les images dans le même dossier où le fichier du document est enregistré. Utiliser`ImagesFolder` pour remplacer ce comportement.

Si vous enregistrez un document dans un flux, Aspose.Words ne dispose pas de dossier pour les images, mais doit néanmoins les enregistrer quelque part. Dans ce cas, vous devez spécifier un dossier accessible dans le`ImagesFolder` propriété.

Si le dossier spécifié par`ImagesFolder` n'existe pas, il sera créé automatiquement.

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
