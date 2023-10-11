---
title: MarkdownSaveOptions.ImagesFolder
second_title: Référence de l'API Aspose.Words pour .NET
description: MarkdownSaveOptions propriété. Spécifie le dossier physique dans lequel les images sont enregistrées lors de lexportation dun document vers leMarkdown format. La valeur par défaut est une chaîne vide.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Spécifie le dossier physique dans lequel les images sont enregistrées lors de l'exportation d'un document vers leMarkdown format. La valeur par défaut est une chaîne vide.

```csharp
public string ImagesFolder { get; set; }
```

### Remarques

Lorsque vous enregistrez un[`Document`](../../../aspose.words/document/) dansMarkdownformat, Aspose.Words doit enregistrer toutes les images intégrées dans le document en tant que fichiers autonomes. `ImagesFolder` permet de préciser où les images seront enregistrées.

Si vous enregistrez un document dans un fichier et fournissez un nom de fichier, Aspose.Words, par défaut, enregistre les images dans le même dossier dans lequel le fichier du document est enregistré. Utiliser`ImagesFolder` pour remplacer ce comportement.

Si vous enregistrez un document dans un flux, Aspose.Words n'a pas de dossier où enregistrer les images, mais doit quand même enregistrer les images quelque part. Dans ce cas, vous devez spécifier un dossier accessible dans le`ImagesFolder` propriété.

Si le dossier spécifié par`ImagesFolder` n'existe pas, il sera créé automatiquement.

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


