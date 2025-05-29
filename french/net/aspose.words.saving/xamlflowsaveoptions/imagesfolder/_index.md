---
title: XamlFlowSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ImagesFolder de XamlFlowSaveOptions vous permet de spécifier facilement un dossier pour enregistrer les images lors de l'exportation de documents au format XAML.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/xamlflowsaveoptions/imagesfolder/
---
## XamlFlowSaveOptions.ImagesFolder property

Spécifie le dossier physique dans lequel les images sont enregistrées lors de l'exportation d'un document au format XAML. La valeur par défaut est une chaîne vide.

```csharp
public string ImagesFolder { get; set; }
```

## Remarques

Lorsque vous enregistrez un[`Document`](../../../aspose.words/document/) au format XAML, Aspose.Words doit enregistrer toutes les images intégrées dans le document en tant que fichiers autonomes.`ImagesFolder` vous permet de spécifier où les images seront enregistrées et[`ImagesFolderAlias`](../imagesfolderalias/) permet de spécifier comment les URI des images seront construits.

Si vous enregistrez un document dans un fichier et fournissez un nom de fichier, Aspose.Words, par défaut, enregistre les images dans le même dossier où le fichier du document est enregistré.`ImagesFolder` pour remplacer ce comportement.

Si vous enregistrez un document dans un flux, Aspose.Words ne dispose pas de dossier d'enregistrement des images ( ), mais doit néanmoins les enregistrer quelque part. Dans ce cas, vous devez spécifier un dossier accessible ( ) dans le`ImagesFolder` propriété ou fournir des flux personnalisés via le[`ImageSavingCallback`](../imagesavingcallback/) gestionnaire d'événements.

## Exemples

Montre comment imprimer les noms de fichiers des images liées créées lors de la conversion d'un document au format .xaml.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Créez un objet « XamlFlowSaveOptions », que nous pouvons transmettre à la méthode « Save » du document
    // pour modifier la façon dont nous enregistrons le document au format d'enregistrement XAML.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Utilisez la propriété « ImagesFolder » pour attribuer un dossier dans le système de fichiers local dans lequel
    // Aspose.Words enregistrera toutes les images liées du document.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Utilisez la propriété « ImagesFolderAlias » pour utiliser ce dossier
    // lors de la construction d'URI d'image au lieu du nom du dossier d'images.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // Un dossier spécifié par « ImagesFolderAlias » devra contenir les ressources au lieu de « ImagesFolder ».
    // Nous devons nous assurer que le dossier existe avant que les flux du rappel puissent y placer leurs ressources.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// Compte et imprime les noms de fichiers des images pendant que leur document parent est converti au format .xaml.
/// </summary>
private class ImageUriPrinter : IImageSavingCallback
{
    public ImageUriPrinter(string imagesFolderAlias)
    {
        ImagesFolderAlias = imagesFolderAlias;
        Resources = new List<string>();
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        Resources.Add(args.ImageFileName);

        // Si nous spécifions un alias de dossier d'images, nous aurions également besoin
        // pour rediriger chaque flux pour mettre son image dans le dossier alias.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Voir également

* class [XamlFlowSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
