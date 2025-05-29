---
title: ResourceSavingArgs.ResourceFileUri
linktitle: ResourceFileUri
articleTitle: ResourceFileUri
second_title: Aspose.Words für .NET
description: Entdecken Sie die ResourceSavingArgs ResourceFileUri-Eigenschaft, um Ressourcendateien in Ihren Dokumenten einfach zu verwalten und zu referenzieren. Steigern Sie noch heute Ihre Effizienz!
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

Mit dieser Eigenschaft können Sie URIs von Ressourcendateien ändern, die in HTML- oder SVG-Dokumente mit festen Seiten exportiert werden.

Aspose.Words generiert beim Export in das HTML- oder SVG-Format mit fester Seite automatisch eine URI für jede Ressourcendatei. Die generierten URIs verweisen auf die von Aspose.Words gespeicherten Ressourcendateien. Die URIs können jedoch fehlerhaft sein, wenn die Ressourcendateien an einen anderen Speicherort verschoben oder in Streams gespeichert werden. Diese Eigenschaft ermöglicht in diesen Fällen die Korrektur der URIs.

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft die von Aspose.Words generierte URI . Sie können den Wert dieser Eigenschaft ändern, um eine benutzerdefinierte URI für die Ressourcendatei bereitzustellen.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

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

* class [ResourceSavingArgs](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
