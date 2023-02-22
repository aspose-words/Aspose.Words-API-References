---
title: ResourceSavingArgs.Document
second_title: Aspose.Words für .NET-API-Referenz
description: ResourceSavingArgs eigendom. Ruft das aktuell gespeicherte Dokumentobjekt ab.
type: docs
weight: 10
url: /de/net/aspose.words.saving/resourcesavingargs/document/
---
## ResourceSavingArgs.Document property

Ruft das aktuell gespeicherte Dokumentobjekt ab.

```csharp
public Document Document { get; }
```

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

### Siehe auch

* class [Document](../../../aspose.words/document/)
* class [ResourceSavingArgs](../)
* namensraum [Aspose.Words.Saving](../../resourcesavingargs/)
* Montage [Aspose.Words](../../../)


