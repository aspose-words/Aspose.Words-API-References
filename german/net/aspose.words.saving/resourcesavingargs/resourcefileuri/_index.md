---
title: ResourceSavingArgs.ResourceFileUri
linktitle: ResourceFileUri
articleTitle: ResourceFileUri
second_title: Aspose.Words für .NET
description: ResourceSavingArgs ResourceFileUri eigendom. Ruft den Uniform Resource Identifier URI ab der zum Verweisen auf die Ressourcendatei aus dem Dokument verwendet wird oder legt diesen fest in C#.
type: docs
weight: 40
url: /de/net/aspose.words.saving/resourcesavingargs/resourcefileuri/
---
## ResourceSavingArgs.ResourceFileUri property

Ruft den Uniform Resource Identifier (URI) ab, der zum Verweisen auf die Ressourcendatei aus dem Dokument verwendet wird, oder legt diesen fest.

```csharp
public string ResourceFileUri { get; set; }
```

## Bemerkungen

Mit dieser Eigenschaft können Sie URIs von Ressourcendateien ändern, die in HTML- oder SVG-Dokumente mit fester Seite exportiert werden.

Aspose.Words generiert beim Export in das feste Seiten-HTML-Format oder SVG automatisch einen URI für jede Ressourcendatei. Die generierten URIs verweisen auf Ressourcendateien, die von Aspose.Words gespeichert wurden. Allerdings können die URIs falsch sein, wenn Ressourcendateien an einen anderen Speicherort verschoben werden sollen oder wenn Ressourcendateien in Streams gespeichert werden. Mit dieser Eigenschaft können in diesen Fällen URIs korrigiert werden.

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft den URI, der von Aspose.Words generiert wurde. Sie können den Wert dieser Eigenschaft ändern, um einen benutzerdefinierten URI für die Ressourcendatei bereitzustellen.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

## Beispiele

Zeigt, wie Sie einen Rückruf verwenden, um externe Ressourcen zu verfolgen, die beim Konvertieren eines Dokuments in HTML erstellt wurden.

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
    /// Wird aufgerufen, wenn Aspose.Words eine externe Ressource in einer festen HTML- oder SVG-Seite speichert.
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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
