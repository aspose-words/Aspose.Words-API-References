---
title: ResourceSavingArgs.ResourceFileName
second_title: Aspose.Words für .NET-API-Referenz
description: ResourceSavingArgs eigendom. Ruft den Dateinamen ohne Pfad ab unter dem die Ressource gespeichert wird oder legt diesen fest.
type: docs
weight: 30
url: /de/net/aspose.words.saving/resourcesavingargs/resourcefilename/
---
## ResourceSavingArgs.ResourceFileName property

Ruft den Dateinamen (ohne Pfad) ab, unter dem die Ressource gespeichert wird, oder legt diesen fest.

```csharp
public string ResourceFileName { get; set; }
```

### Bemerkungen

Mit dieser Eigenschaft können Sie neu definieren, wie die Ressourcendateinamen beim Export in feste Seiten-HTML oder SVG generiert werden .

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft den Dateinamen, der von Aspose.Words generiert wurde. Sie können den Wert dieser Eigenschaft ändern, um die Ressource in einer anderen Datei zu speichern. Beachten Sie, dass Dateinamen eindeutig sein müssen.

Aspose.Words generiert automatisch einen eindeutigen Dateinamen für jede Ressource, wenn in das feste Seiten-HTML- oder SVG-Format exportiert wird. Wie der Ressourcendateiname generiert wird, hängt davon ab, ob Sie das Dokument in einer Datei oder in einem Stream speichern.

Beim Speichern eines Dokuments in einer Datei sieht der generierte Ressourcendateiname wie folgt aus: &lt;Name der Basisdatei des Dokuments&gt;.&lt;Bildnummer&gt;.&lt;Erweiterung&gt;.

Beim Speichern eines Dokuments in einem Stream sieht der generierte Ressourcendateiname wie folgt aus: Aspose.Words.&lt;Dokument-Guid&gt;.&lt;Bildnummer&gt;.&lt;Erweiterung&gt;.

`ResourceFileName` darf nur den Dateinamen ohne den Pfad enthalten. Aspose.Words bestimmt den Pfad zum Speichern und den Wert des`src` Attribut zum Schreiben von in festes Seiten-HTML oder SVG unter Verwendung des Dokumentdateinamens[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/) oder[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/) Und[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/) oder[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/) Eigenschaften.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

### Beispiele

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
* namensraum [Aspose.Words.Saving](../../resourcesavingargs/)
* Montage [Aspose.Words](../../../)


