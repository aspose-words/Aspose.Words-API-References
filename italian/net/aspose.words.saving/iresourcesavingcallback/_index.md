---
title: Interface IResourceSavingCallback
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.IResourceSavingCallback interfaccia. Implementa questa interfaccia se vuoi controllare come Aspose.Words salva risorse esterne immagini caratteri e CSS quando salva un documento in una pagina fissa HTML o SVG.
type: docs
weight: 5190
url: /it/net/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface

Implementa questa interfaccia se vuoi controllare come Aspose.Words salva risorse esterne (immagini, caratteri e CSS) quando salva un documento in una pagina fissa HTML o SVG.

```csharp
public interface IResourceSavingCallback
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ResourceSaving](../../aspose.words.saving/iresourcesavingcallback/resourcesaving/)(ResourceSavingArgs) | Chiamato quando Aspose.Words salva una risorsa esterna nei formati HTML o SVG a pagina fissa. |

### Esempi

Mostra come utilizzare un callback per tenere traccia delle risorse esterne create durante la conversione di un documento in HTML.

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
    /// Chiamato quando Aspose.Words salva una risorsa esterna su una pagina HTML o SVG fissa.
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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


