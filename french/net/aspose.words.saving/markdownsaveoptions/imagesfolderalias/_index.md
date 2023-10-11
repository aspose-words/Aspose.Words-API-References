---
title: MarkdownSaveOptions.ImagesFolderAlias
second_title: Référence de l'API Aspose.Words pour .NET
description: MarkdownSaveOptions propriété. Spécifie le nom du dossier utilisé pour construire les URI dimage écrits dans un document. La valeur par défaut est une chaîne vide.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Spécifie le nom du dossier utilisé pour construire les URI d'image écrits dans un document. La valeur par défaut est une chaîne vide.

```csharp
public string ImagesFolderAlias { get; set; }
```

### Remarques

Lorsque vous enregistrez un[`Document`](../../../aspose.words/document/) dansMarkdown format, Aspose.Words doit enregistrer toutes les images intégrées dans le document en tant que fichiers autonomes. [`ImagesFolder`](../imagesfolder/) permet de préciser où les images seront enregistrées et `ImagesFolderAlias` permet de spécifier comment les URI des images seront construites.

Si`ImagesFolderAlias` n'est pas une chaîne vide, alors l'URI de l'image written vers Markdown seraImagesFolderAlias + &lt;nom du fichier image&gt;.

Si`ImagesFolderAlias` est une chaîne vide, alors l'URI de l'image written vers Markdown seraImagesFolder + &lt;nom du fichier image&gt;.

Si`ImagesFolderAlias`est réglé sur '.' (point), alors le fichier image name sera écrit dans Markdown sans chemin, quelles que soient les autres options.

### Exemples

Montre comment spécifier le nom du dossier utilisé pour construire les URI d’image.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
Image image = Image.FromFile(ImageDir + "Logo.jpg");
builder.InsertImage(image);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Utilisez la propriété "ImagesFolder" pour attribuer un dossier dans le système de fichiers local dans lequel
// Aspose.Words enregistrera toutes les images liées au document.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// Utilisez la propriété "ImagesFolderAlias" pour utiliser ce dossier
// lors de la construction des URI d'image au lieu du nom du dossier images.
saveOptions.ImagesFolderAlias = "http://exemple.com/images" ;

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

Montre comment spécifier le nom du dossier utilisé pour construire les URI d’image (.NetStandard 2.0).

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(bitmap);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Utilisez la propriété "ImagesFolder" pour attribuer un dossier dans le système de fichiers local dans lequel
// Aspose.Words enregistrera toutes les images liées au document.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// Utilisez la propriété "ImagesFolderAlias" pour utiliser ce dossier
// lors de la construction des URI d'image au lieu du nom du dossier images.
saveOptions.ImagesFolderAlias = "http://exemple.com/images" ;

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### Voir également

* class [MarkdownSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../markdownsaveoptions/)
* Assemblée [Aspose.Words](../../../)


