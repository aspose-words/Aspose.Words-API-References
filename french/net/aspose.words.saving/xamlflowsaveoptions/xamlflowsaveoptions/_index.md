---
title: XamlFlowSaveOptions
linktitle: XamlFlowSaveOptions
articleTitle: XamlFlowSaveOptions
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur XamlFlowSaveOptions pour initialiser et enregistrer facilement des documents au format XamlFlow. Améliorez votre flux de travail dès aujourd'hui !
type: docs
weight: 10
url: /fr/net/aspose.words.saving/xamlflowsaveoptions/xamlflowsaveoptions/
---
## XamlFlowSaveOptions() {#constructor}

Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leXamlFlow format.

```csharp
public XamlFlowSaveOptions()
```

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

---

## XamlFlowSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leXamlFlow ouXamlFlowPack format.

```csharp
public XamlFlowSaveOptions(SaveFormat saveFormat)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| saveFormat | SaveFormat | Peut êtreXamlFlow ouXamlFlowPack. |

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XamlFlowSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
