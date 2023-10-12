---
title: HtmlFixedSaveOptions.ResourcesFolder
second_title: Aspose.Words per .NET API Reference
description: HtmlFixedSaveOptions proprietà. Specifica la cartella fisica in cui vengono salvate le risorse immagini caratteri css durante lesportazione di un documento in formato Html. Il valore predefinito ènullo .
type: docs
weight: 140
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/
---
## HtmlFixedSaveOptions.ResourcesFolder property

Specifica la cartella fisica in cui vengono salvate le risorse (immagini, caratteri, css) durante l'esportazione di un documento in formato Html. Il valore predefinito è`nullo` .

```csharp
public string ResourcesFolder { get; set; }
```

### Osservazioni

Ha effetto solo se[`ExportEmbeddedImages`](../exportembeddedimages/) la proprietà è`falso`.

Quando salvi un file[`Document`](../../../aspose.words/document/) in formato Html, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi.`ResourcesFolder` ti consente di specificare dove verranno salvate le immagini e[`ResourcesFolderAlias`](../resourcesfolderalias/) consente di specificare come verranno costruiti gli URI dell'immagine.

Se salvi un documento in un file e fornisci un nome file, Aspose.Words, per impostazione predefinita, salva le immagini nella stessa cartella in cui è salvato il file del documento. Utilizzo`ResourcesFolder` per sovrascrivere questo comportamento.

Se salvi un documento in uno stream, Aspose.Words non ha una cartella in cui salvare le immagini, ma deve comunque salvare le immagini da qualche parte. In questo caso, è necessario specificare una cartella accessibile utilizzando il file`ResourcesFolder` proprietà

### Esempi

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
    // Dobbiamo garantire che la cartella esista prima che i flussi possano inserirvi le proprie risorse.
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
                // Per impostazione predefinita, "ResourceFileUri" utilizza la cartella di sistema per i caratteri.
                // Per evitare problemi su altre piattaforme è necessario specificare esplicitamente il percorso dei caratteri.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // Se abbiamo specificato una cartella nella proprietà "ResourcesFolderAlias",
        // dovremo anche reindirizzare ogni flusso per inserire la relativa risorsa in quella cartella.
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

* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* assemblea [Aspose.Words](../../../)


