---
title: ResourceSavingArgs.KeepResourceStreamOpen
linktitle: KeepResourceStreamOpen
articleTitle: KeepResourceStreamOpen
second_title: Aspose.Words per .NET
description: Scopri come la proprietà KeepResourceStreamOpen in ResourceSavingArgs migliora Aspose.Words gestendo l'efficienza del flusso durante il risparmio delle risorse.
type: docs
weight: 20
url: /it/net/aspose.words.saving/resourcesavingargs/keepresourcestreamopen/
---
## ResourceSavingArgs.KeepResourceStreamOpen property

Specifica se Aspose.Words deve mantenere aperto il flusso o chiuderlo dopo aver salvato una risorsa.

```csharp
public bool KeepResourceStreamOpen { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` e Aspose.Words chiuderà il flusso fornito nel[`ResourceStream`](../resourcestream/) proprietà dopo aver scritto una risorsa in essa. Specificare`VERO` per mantenere aperto il flusso.

## Esempi

Mostra come utilizzare un callback per stampare gli URI delle risorse esterne create durante la conversione di un documento in HTML.

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

    // Una cartella specificata da ResourcesFolderAlias conterrà le risorse anziché ResourcesFolder.
    // Dobbiamo assicurarci che la cartella esista prima che i flussi possano inserirvi le loro risorse.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Conta e stampa gli URI delle risorse contenute da mentre vengono convertiti in HTML fisso.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // Se impostiamo un alias di cartella nell'oggetto SaveOptions, potremo stamparlo da qui.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // Per impostazione predefinita, 'ResourceFileUri' utilizza la cartella di sistema per i font.
                // Per evitare problemi su altre piattaforme è necessario specificare esplicitamente il percorso per i font.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // Se abbiamo specificato una cartella nella proprietà "ResourcesFolderAlias",
        // dovremo anche reindirizzare ogni flusso per mettere la sua risorsa in quella cartella.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### Guarda anche

* class [ResourceSavingArgs](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
