---
title: XamlFixedSaveOptions.SaveFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: XamlFixedSaveOptions propriété. Spécifie le format dans lequel le document sera enregistré si cet objet doptions denregistrement est utilisé. Ne peut êtreXamlFixed .
type: docs
weight: 50
url: /fr/net/aspose.words.saving/xamlfixedsaveoptions/saveformat/
---
## XamlFixedSaveOptions.SaveFormat property

Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut êtreXamlFixed .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Exemples

Montre comment imprimer les URI des ressources liées créées lors de la conversion d'un document en .xaml de forme fixe.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Crée un objet "XamlFixedSaveOptions", que nous pouvons passer à la méthode "Save" du document
    // pour modifier la façon dont nous enregistrons le document au format d'enregistrement XAML.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Utilisez la propriété "ResourcesFolder" pour affecter un dossier dans le système de fichiers local dans lequel
    // Aspose.Words enregistrera toutes les ressources liées du document, telles que les images et les polices.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Utilisez la propriété "ResourcesFolderAlias" pour utiliser ce dossier
    // lors de la construction d'URI d'image au lieu du nom du dossier de ressources.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // Un dossier spécifié par "ResourcesFolderAlias" devra contenir les ressources au lieu de "ResourcesFolder".
    // Nous devons nous assurer que le dossier existe avant que les flux du rappel puissent y mettre leurs ressources.
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

        // Si nous avons spécifié un alias de dossier de ressources, nous aurions également besoin
        // pour rediriger chaque flux pour mettre sa ressource dans le dossier alias.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XamlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../xamlfixedsaveoptions/)
* Assemblée [Aspose.Words](../../../)


