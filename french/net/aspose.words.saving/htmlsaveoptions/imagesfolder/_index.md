---
title: HtmlSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ImagesFolder de HtmlSaveOptions. Définissez facilement le dossier d'enregistrement des images lors de l'exportation de documents au format HTML. Simplifiez votre flux de travail dès aujourd'hui !
type: docs
weight: 360
url: /fr/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

Spécifie le dossier physique dans lequel les images sont enregistrées lors de l'exportation d'un document au format HTML. La valeur par défaut est une chaîne vide.

```csharp
public string ImagesFolder { get; set; }
```

## Remarques

Lorsque vous enregistrez un[`Document`](../../../aspose.words/document/) au format HTML, Aspose.Words doit enregistrer toutes les images intégrées dans le document sous forme de fichiers autonomes.`ImagesFolder` vous permet de spécifier où les images seront enregistrées et[`ImagesFolderAlias`](../imagesfolderalias/) permet de spécifier comment les URI des images seront construits.

Si vous enregistrez un document dans un fichier et fournissez un nom de fichier, Aspose.Words, par défaut, enregistre les images dans le même dossier où le fichier du document est enregistré.`ImagesFolder` pour remplacer ce comportement.

Si vous enregistrez un document dans un flux, Aspose.Words ne dispose pas de dossier pour enregistrer les images, mais doit tout de même les enregistrer quelque part. Dans ce cas, vous devez spécifier un dossier accessible dans le fichier`ImagesFolder` propriété ou fournir des flux personnalisés via le[`ImageSavingCallback`](../imagesavingcallback/) gestionnaire d'événements.

Si le dossier spécifié par`ImagesFolder` n'existe pas, il sera créé automatiquement.

[`ResourceFolder`](../resourcefolder/) est une autre façon de spécifier un dossier dans lequel les images doivent être enregistrées.

## Exemples

Montre comment spécifier le dossier pour stocker les images liées après l'enregistrement au format .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Définissez une option pour exporter les champs de formulaire sous forme de texte brut au lieu d'éléments d'entrée HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
