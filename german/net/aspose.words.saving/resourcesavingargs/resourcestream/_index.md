---
title: ResourceSavingArgs.ResourceStream
linktitle: ResourceStream
articleTitle: ResourceStream
second_title: Aspose.Words für .NET
description: Entdecken Sie die ResourceSavingArgs ResourceStream-Eigenschaft, um einfach zu definieren, wo Ihre Ressourcen gespeichert werden, und so die Effizienz und Kontrolle Ihrer Projekte zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words.saving/resourcesavingargs/resourcestream/
---
## ResourceSavingArgs.ResourceStream property

Ermöglicht die Angabe des Streams, in dem die Ressource gespeichert wird.

```csharp
public Stream ResourceStream { get; set; }
```

## Bemerkungen

Mit dieser Eigenschaft können Sie Ressourcen in Streams statt in Dateien speichern.

Der Standardwert ist`null` Wenn diese Eigenschaft`null` wird die Ressource in einer Datei gespeichert, die in der[`ResourceFileName`](../resourcefilename/) Eigentum.

Verwenden[`IResourceSavingCallback`](../../iresourcesavingcallback/) Sie können eine Ressource nicht durch eine andere ersetzen. Es dient nur der Kontrolle über den Speicherort der Ressourcen.

## Beispiele

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
    // Wir müssen sicherstellen, dass der Ordner vorhanden ist, bevor die Streams ihre Ressourcen darin ablegen können.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Zählt und druckt URIs der enthaltenen Ressourcen, wenn sie in festes HTML konvertiert werden.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // Wenn wir im SaveOptions-Objekt einen Ordneralias festlegen, können wir ihn von hier aus drucken.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // Standardmäßig verwendet „ResourceFileUri“ den Systemordner für Schriftarten.
                // Um Probleme auf anderen Plattformen zu vermeiden, müssen Sie den Pfad für die Schriftarten explizit angeben.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // Wenn wir in der Eigenschaft „ResourcesFolderAlias“ einen Ordner angegeben haben,
        // Wir müssen auch jeden Stream umleiten, um seine Ressource in diesem Ordner abzulegen.
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

* class [ResourceSavingArgs](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
