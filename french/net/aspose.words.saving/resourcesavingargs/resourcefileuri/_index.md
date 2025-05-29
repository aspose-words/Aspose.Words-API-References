---
title: ResourceSavingArgs.ResourceFileUri
linktitle: ResourceFileUri
articleTitle: ResourceFileUri
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ResourceSavingArgs ResourceFileUri pour gérer et référencer facilement les fichiers de ressources dans vos documents. Gagnez en efficacité dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words.saving/resourcesavingargs/resourcefileuri/
---
## ResourceSavingArgs.ResourceFileUri property

Obtient ou définit l'identifiant de ressource uniforme (URI) utilisé pour référencer le fichier de ressources à partir du document.

```csharp
public string ResourceFileUri { get; set; }
```

## Remarques

Cette propriété vous permet de modifier les URI des fichiers de ressources exportés vers des documents HTML ou SVG à page fixe.

Aspose.Words génère automatiquement une URI pour chaque fichier de ressources lors de l'exportation au format HTML ou SVG. Les URI générées font référence aux fichiers de ressources enregistrés par Aspose.Words. Cependant, les URI peuvent être incorrects si les fichiers de ressources doivent être déplacés vers un autre emplacement ou enregistrés dans des flux. Cette propriété permet de corriger les URI dans ces cas.

Lorsque l'événement est déclenché, cette propriété contient l'URI générée par Aspose.Words. Vous pouvez modifier la valeur de cette propriété pour fournir une URI personnalisée pour le fichier de ressources.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

## Exemples

Montre comment utiliser un rappel pour suivre les ressources externes créées lors de la conversion d'un document en HTML.

```csharp
public void ResourceSavingCallback()
{
    Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

    FontSavingCallback callback = new FontSavingCallback();

    HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
    {
        ResourceSavingCallback = callback
    };

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

    Console.WriteLine(callback.GetText());
}

private class FontSavingCallback : IResourceSavingCallback
{
    /// <summary>
    /// Appelé lorsque Aspose.Words enregistre une ressource externe dans une page fixe HTML ou SVG.
    /// </summary>
    public void ResourceSaving(ResourceSavingArgs args)
    {
        mText.AppendLine($"Original document URI:\t{args.Document.OriginalFileName}");
        mText.AppendLine($"Resource being saved:\t{args.ResourceFileName}");
        mText.AppendLine($"Full uri after saving:\t{args.ResourceFileUri}\n");
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private readonly StringBuilder mText = new StringBuilder();
}
```

### Voir également

* class [ResourceSavingArgs](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
