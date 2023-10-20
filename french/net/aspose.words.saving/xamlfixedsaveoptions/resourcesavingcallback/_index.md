---
title: XamlFixedSaveOptions.ResourceSavingCallback
linktitle: ResourceSavingCallback
articleTitle: ResourceSavingCallback
second_title: Aspose.Words pour .NET
description: XamlFixedSaveOptions ResourceSavingCallback propriété. Permet de contrôler la manière dont les ressources images et polices sont enregistrées lorsquun document est exporté au format Xaml de page fixe en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/xamlfixedsaveoptions/resourcesavingcallback/
---
## XamlFixedSaveOptions.ResourceSavingCallback property

Permet de contrôler la manière dont les ressources (images et polices) sont enregistrées lorsqu'un document est exporté au format Xaml de page fixe.

```csharp
public IResourceSavingCallback ResourceSavingCallback { get; set; }
```

## Exemples

Montre comment imprimer les URI des ressources liées créées lors de la conversion d'un document en .xaml de forme fixe.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Crée un objet "XamlFixedSaveOptions", que l'on peut passer à la méthode "Save" du document
    // pour modifier la façon dont nous enregistrons le document au format de sauvegarde XAML.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Utilisez la propriété "ResourcesFolder" pour attribuer un dossier dans le système de fichiers local dans lequel
    // Aspose.Words enregistrera toutes les ressources liées au document, telles que les images et les polices.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Utilisez la propriété "ResourcesFolderAlias" pour utiliser ce dossier
    // lors de la construction des URI d'image au lieu du nom du dossier de ressources.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // Un dossier spécifié par "ResourcesFolderAlias" devra contenir les ressources au lieu de "ResourcesFolder".
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
        // pour rediriger chaque flux pour mettre sa ressource dans le dossier alias.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Voir également

* interface [IResourceSavingCallback](../../iresourcesavingcallback/)
* class [XamlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
