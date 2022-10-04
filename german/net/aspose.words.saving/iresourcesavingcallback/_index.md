---
title: IResourceSavingCallback
second_title: Aspose.Words für .NET-API-Referenz
description: Implementieren Sie diese Schnittstelle wenn Sie steuern möchten wie Aspose.Words externe Ressourcen Bilder Schriftarten und CSS speichert wenn ein Dokument als HTML oder SVG mit fester Seite gespeichert wird.
type: docs
weight: 4930
url: /de/net/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface

Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie Aspose.Words externe Ressourcen (Bilder, Schriftarten und CSS) speichert, wenn ein Dokument als HTML oder SVG mit fester Seite gespeichert wird.

```csharp
public interface IResourceSavingCallback
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ResourceSaving](../../aspose.words.saving/iresourcesavingcallback/resourcesaving/)(ResourceSavingArgs) | Wird aufgerufen, wenn Aspose.Words eine externe Ressource in HTML- oder SVG-Formaten mit festen Seiten speichert. |

### Beispiele

Zeigt, wie ein Rückruf verwendet wird, um externe Ressourcen nachzuverfolgen, die beim Konvertieren eines Dokuments in HTML erstellt wurden.

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
    /// Wird aufgerufen, wenn Aspose.Words eine externe Ressource in HTML oder SVG für feste Seiten speichert.
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

Zeigt, wie ein Rückruf verwendet wird, um die URIs externer Ressourcen zu drucken, die beim Konvertieren eines Dokuments in HTML erstellt wurden.

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

    // Ein durch ResourcesFolderAlias angegebener Ordner enthält die Ressourcen anstelle von ResourcesFolder.
    // Wir müssen sicherstellen, dass der Ordner existiert, bevor die Streams ihre Ressourcen darin ablegen können.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Zählt und druckt URIs von Ressourcen, die in enthalten sind, während sie in festes HTML konvertiert werden.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // Wenn wir im SaveOptions-Objekt einen Ordner-Alias festlegen, können wir ihn von hier aus drucken.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // Standardmäßig verwendet 'ResourceFileUri' den Systemordner für Schriftarten.
                // Um Probleme auf anderen Plattformen zu vermeiden, müssen Sie den Pfad für die Schriftarten explizit angeben.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // Wenn wir in der Eigenschaft "ResourcesFolderAlias" einen Ordner angegeben haben,
        // Wir müssen auch jeden Stream umleiten, um seine Ressource in diesen Ordner zu legen.
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

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
