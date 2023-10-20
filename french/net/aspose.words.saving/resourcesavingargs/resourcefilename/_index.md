---
title: ResourceSavingArgs.ResourceFileName
linktitle: ResourceFileName
articleTitle: ResourceFileName
second_title: Aspose.Words pour .NET
description: ResourceSavingArgs ResourceFileName propriété. Obtient ou définit le nom du fichier sans chemin dans lequel la ressource sera enregistrée en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/resourcesavingargs/resourcefilename/
---
## ResourceSavingArgs.ResourceFileName property

Obtient ou définit le nom du fichier (sans chemin) dans lequel la ressource sera enregistrée.

```csharp
public string ResourceFileName { get; set; }
```

## Remarques

Cette propriété vous permet de redéfinir la manière dont les noms de fichiers de ressources sont générés lors de l'exportation vers une page fixe HTML ou SVG.

Lorsque l'événement est déclenché, cette propriété contient le nom de fichier généré par Aspose.Words. Vous pouvez modifier la valeur de cette propriété pour enregistrer la ressource dans un fichier différent. Notez que les noms de fichiers doivent être uniques.

Aspose.Words génère automatiquement un nom de fichier unique pour chaque ressource lors de l'exportation au format HTML ou SVG de page fixe. La manière dont le nom du fichier de ressources est généré dépend du fait que vous enregistrez le document dans un fichier ou dans un flux.

Lors de l'enregistrement d'un document dans un fichier, le nom du fichier de ressources généré ressemble à &lt;nom du fichier de base du document&gt;.&lt;numéro d'image&gt;.&lt;extension&gt;.

Lors de l'enregistrement d'un document dans un flux, le nom du fichier de ressources généré ressemble à Aspose.Words.&lt;guid du document&gt;.&lt;numéro d'image&gt;.&lt;extension&gt;.

`ResourceFileName` doit contenir uniquement le nom du fichier sans le chemin. Aspose.Words détermine le chemin de sauvegarde et la valeur du`src` attribut pour écrire sur une page HTML ou SVG fixe en utilisant le nom du fichier du document, le[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/) ou[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/) et[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/) ou[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/) propriétés.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

## Exemples

Montre comment utiliser un rappel pour suivre les ressources externes créées lors de la conversion d'un document au format HTML.

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
    /// Appelé lorsque Aspose.Words enregistre une ressource externe dans une page HTML ou SVG fixe.
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
