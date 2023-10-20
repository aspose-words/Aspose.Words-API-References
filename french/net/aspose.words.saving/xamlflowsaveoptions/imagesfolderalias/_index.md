---
title: XamlFlowSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words pour .NET
description: XamlFlowSaveOptions ImagesFolderAlias propriété. Spécifie le nom du dossier utilisé pour construire les URI dimage écrits dans un document XAML. La valeur par défaut est une chaîne vide en C#.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/
---
## XamlFlowSaveOptions.ImagesFolderAlias property

Spécifie le nom du dossier utilisé pour construire les URI d'image écrits dans un document XAML. La valeur par défaut est une chaîne vide.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Remarques

Lorsque vous enregistrez un[`Document`](../../../aspose.words/document/) au format XAML, Aspose.Words doit enregistrer toutes les images intégrées dans le document en tant que fichiers autonomes.[`ImagesFolder`](../imagesfolder/) permet de préciser où les images seront enregistrées et`ImagesFolderAlias` permet de spécifier comment les URI des images seront construites.

Si`ImagesFolderAlias` n'est pas une chaîne vide, alors l'URI de l'image written en XAML seraImagesFolderAlias + &lt;nom du fichier image&gt;.

Si`ImagesFolderAlias`est une chaîne vide, alors l'URI de l'image écrite en XAML seraImagesFolder + &lt;nom du fichier image&gt;.

Si`ImagesFolderAlias` est réglé sur '.' (point), le nom du fichier image sera écrit en XAML sans chemin, quelles que soient les autres options.

## Exemples

Montre comment imprimer les noms de fichiers des images liées créées lors de la conversion d'un document en .xaml sous forme de flux.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Crée un objet "XamlFlowSaveOptions", que l'on peut passer à la méthode "Save" du document
    // pour modifier la façon dont nous enregistrons le document au format de sauvegarde XAML.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Utilisez la propriété "ImagesFolder" pour attribuer un dossier dans le système de fichiers local dans lequel
    // Aspose.Words enregistrera toutes les images liées au document.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Utilisez la propriété "ImagesFolderAlias" pour utiliser ce dossier
    // lors de la construction des URI d'image au lieu du nom du dossier images.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // Un dossier spécifié par "ImagesFolderAlias" devra contenir les ressources au lieu de "ImagesFolder".
    // Nous devons nous assurer que le dossier existe avant que les flux du rappel puissent y placer leurs ressources.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// Compte et imprime les noms de fichiers des images pendant que leur document parent est converti en flux .xaml.
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

        // Si nous spécifions un alias de dossier image, nous aurions également besoin
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
