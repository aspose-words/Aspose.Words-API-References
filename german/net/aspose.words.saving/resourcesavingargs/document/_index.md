---
title: ResourceSavingArgs.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words für .NET
description: Entdecken Sie die Document-Eigenschaft ResourceSavingArgs, um auf das aktuell gespeicherte Dokumentobjekt zuzugreifen und so die Effizienz Ihres Workflows zu steigern.
type: docs
weight: 10
url: /de/net/aspose.words.saving/resourcesavingargs/document/
---
## ResourceSavingArgs.Document property

Ruft das Dokumentobjekt ab, das aktuell gespeichert wird.

```csharp
public Document Document { get; }
```

## Beispiele

Zeigt, wie ein Rückruf verwendet wird, um externe Ressourcen zu verfolgen, die beim Konvertieren eines Dokuments in HTML erstellt wurden.

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
    /// Wird aufgerufen, wenn Aspose.Words eine externe Ressource in festem Seiten-HTML oder SVG speichert.
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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
