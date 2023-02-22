---
title: ResourceSavingArgs.ResourceFileUri
second_title: Aspose.Words für .NET-API-Referenz
description: ResourceSavingArgs eigendom. Ruft den Uniform Resource Identifier URI ab oder legt ihn fest der zum Verweisen auf die Ressourcendatei aus dem Dokument verwendet wird.
type: docs
weight: 40
url: /de/net/aspose.words.saving/resourcesavingargs/resourcefileuri/
---
## ResourceSavingArgs.ResourceFileUri property

Ruft den Uniform Resource Identifier (URI) ab oder legt ihn fest, der zum Verweisen auf die Ressourcendatei aus dem Dokument verwendet wird.

```csharp
public string ResourceFileUri { get; set; }
```

### Bemerkungen

Mit dieser Eigenschaft können Sie URIs von Ressourcendateien ändern, die in HTML- oder SVG-Dokumente mit festen Seiten exportiert wurden.

Aspose.Words generiert automatisch einen URI für jede Ressourcendatei während des Exports in das HTML - oder SVG-Format mit festen Seiten. Die generierten URIs verweisen auf Ressourcendateien, die von Aspose.Words gespeichert wurden. Die URIs können jedoch falsch sein, wenn Ressourcendateien an einen anderen Ort verschoben oder Ressourcendateien in Streams gespeichert werden. Diese Eigenschaft ermöglicht es, URIs in diesen Fällen zu korrigieren.

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft den URI, der von Aspose.Words generiert wurde. Sie können den Wert dieser Eigenschaft ändern, um einen benutzerdefinierten URI für die Ressourcendatei bereitzustellen.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

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

* class [ResourceSavingArgs](../)
* namensraum [Aspose.Words.Saving](../../resourcesavingargs/)
* Montage [Aspose.Words](../../../)


