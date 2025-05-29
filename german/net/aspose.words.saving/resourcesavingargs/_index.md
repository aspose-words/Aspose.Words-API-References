---
title: ResourceSavingArgs Class
linktitle: ResourceSavingArgs
articleTitle: ResourceSavingArgs
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Saving.ResourceSavingArgs, die Ihre Dokumentverarbeitung verbessert, indem sie wichtige Daten für das ResourceSaving-Ereignis bereitstellt.
type: docs
weight: 6360
url: /de/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

Liefert Daten für die[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) Ereignis.

Um mehr zu erfahren, besuchen Sie die[Speichern eines Dokuments](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

```csharp
public class ResourceSavingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | Ruft das Dokumentobjekt ab, das aktuell gespeichert wird. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | Gibt an, ob Aspose.Words den Stream nach dem Speichern einer Ressource geöffnet halten oder schließen soll. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | Ruft den Dateinamen (ohne Pfad) ab oder legt ihn fest, unter dem die Ressource gespeichert wird. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | Ruft den Uniform Resource Identifier (URI) ab, der zum Verweisen auf die Ressourcendatei aus dem Dokument verwendet wird, oder legt diesen fest. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | Ermöglicht die Angabe des Streams, in dem die Ressource gespeichert wird. |

## Bemerkungen

Wenn Aspose.Words ein Dokument als festes HTML oder SVG speichert, speichert es standardmäßig jede Ressource in einer separaten Datei. Aspose.Words verwendet den Dateinamen des Dokuments und eine eindeutige Nummer, um für jede im Dokument gefundene Ressource einen eindeutigen Dateinamen zu generieren.

`ResourceSavingArgs` ermöglicht es, die Generierung von Ressourcendateinamen neu zu definieren oder das Speichern von Ressourcen in Dateien vollständig zu umgehen, indem Sie eigene Stream-Objekte bereitstellen.

Um Ihre eigene Logik zum Generieren von Ressourcendateinamen anzuwenden, verwenden Sie [`ResourceFileName`](./resourcefilename/) Eigentum.

Um Ressourcen in Streams statt in Dateien zu speichern, verwenden Sie die[`ResourceStream`](./resourcestream/) Eigentum.

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
