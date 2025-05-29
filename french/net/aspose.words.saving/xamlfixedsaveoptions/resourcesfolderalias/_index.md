---
title: XamlFixedSaveOptions.ResourcesFolderAlias
linktitle: ResourcesFolderAlias
articleTitle: ResourcesFolderAlias
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ResourcesFolderAlias de XamlFixedSaveOptions améliore la gestion des URI d'images dans les documents Xaml. Optimisez vos mises en page fixes dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words.saving/xamlfixedsaveoptions/resourcesfolderalias/
---
## XamlFixedSaveOptions.ResourcesFolderAlias property

Spécifie le nom du dossier utilisé pour construire les URI d'image écrites dans un document Xaml à page fixe. La valeur par défaut est`nul` .

```csharp
public string ResourcesFolderAlias { get; set; }
```

## Remarques

Lorsque vous enregistrez un[`Document`](../../../aspose.words/document/) au format Xaml à page fixe, Aspose.Words doit enregistrer toutes les images intégrées dans le document sous forme de fichiers autonomes.[`ResourcesFolder`](../resourcesfolder/) vous permet de spécifier où les images seront enregistrées et`ResourcesFolderAlias` permet de spécifier comment les URI des images seront construits.

## Exemples

Montre comment imprimer les URI des ressources liées créées lors de la conversion d'un document au format .xaml fixe.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Créez un objet « XamlFixedSaveOptions », que nous pouvons transmettre à la méthode « Save » du document
    // pour modifier la façon dont nous enregistrons le document au format d'enregistrement XAML.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Utilisez la propriété « ResourcesFolder » pour attribuer un dossier dans le système de fichiers local dans lequel
    // Aspose.Words enregistrera toutes les ressources liées au document, telles que les images et les polices.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Utilisez la propriété « ResourcesFolderAlias » pour utiliser ce dossier
    // lors de la construction d'URI d'image au lieu du nom du dossier de ressources.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // Un dossier spécifié par « ResourcesFolderAlias » devra contenir les ressources au lieu de « ResourcesFolder ».
    // Nous devons nous assurer que le dossier existe avant que les flux du rappel puissent y placer leurs ressources.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// Compte et imprime les URI des ressources créées lors de la conversion en .xaml fixe.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    public ResourceUriPrinter()
    {
        Resources = new List<string>();
    }

    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Resources.Add($"Resource \"{args.ResourceFileName}\"\n\t{args.ResourceFileUri}");

        // Si nous spécifions un alias de dossier de ressources, nous aurions également besoin
        // pour rediriger chaque flux pour placer sa ressource dans le dossier alias.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Voir également

* class [XamlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
