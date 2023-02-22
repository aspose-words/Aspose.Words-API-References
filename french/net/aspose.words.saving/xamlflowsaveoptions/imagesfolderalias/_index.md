---
title: XamlFlowSaveOptions.ImagesFolderAlias
second_title: Référence de l'API Aspose.Words pour .NET
description: XamlFlowSaveOptions propriété. Spécifie le nom du dossier utilisé pour construire les URI dimage écrites dans un document XAML. La valeur par défaut est une chaîne vide.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/
---
## XamlFlowSaveOptions.ImagesFolderAlias property

Spécifie le nom du dossier utilisé pour construire les URI d'image écrites dans un document XAML. La valeur par défaut est une chaîne vide.

```csharp
public string ImagesFolderAlias { get; set; }
```

### Remarques

Lorsque vous enregistrez un[`Document`](../../../aspose.words/document/) au format XAML, Aspose.Words doit enregistrer toutes les images incorporées dans le document en tant que fichiers autonomes.[`ImagesFolder`](../imagesfolder/) vous permet de spécifier où les images seront enregistrées et`ImagesFolderAlias` permet de spécifier comment les URI des images seront construites.

Si`ImagesFolderAlias` n'est pas une chaîne vide, alors l'URI de l'image écrite en XAML seraImagesFolderAlias + &lt;nom du fichier image&gt;.

Si`ImagesFolderAlias` est une chaîne vide, alors l'URI de l'image écrite en XAML seraImagesFolder + &lt;nom du fichier image&gt;.

Si`ImagesFolderAlias` est réglé sur '.' (point), le nom du fichier image sera écrit en XAML sans chemin, quelles que soient les autres options.

### Exemples

Montre comment imprimer les noms de fichiers des images liées créées lors de la conversion d'un document en flux .xaml.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Crée un objet "XamlFlowSaveOptions", que nous pouvons passer à la méthode "Save" du document
    // pour modifier la façon dont nous enregistrons le document au format d'enregistrement XAML.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Utilisez la propriété "ImagesFolder" pour affecter un dossier dans le système de fichiers local dans lequel
    // Aspose.Words enregistrera toutes les images liées du document.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Utilisez la propriété "ImagesFolderAlias" pour utiliser ce dossier
    // lors de la construction d'URI d'image au lieu du nom du dossier d'images.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // Un dossier spécifié par "ImagesFolderAlias" devra contenir les ressources au lieu de "ImagesFolder".
    // Nous devons nous assurer que le dossier existe avant que les flux du rappel puissent y mettre leurs ressources.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");

/// <summary>
/// Compte et imprime les noms de fichiers des images pendant que leur document parent est converti en flux de forme .xaml.
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

        // Si nous avons spécifié un alias de dossier d'image, nous aurions également besoin
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
* espace de noms [Aspose.Words.Saving](../../xamlflowsaveoptions/)
* Assemblée [Aspose.Words](../../../)


