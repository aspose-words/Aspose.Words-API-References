---
title: ResourceSavingArgs Class
linktitle: ResourceSavingArgs
articleTitle: ResourceSavingArgs
second_title: Aspose.Words für .NET
description: Aspose.Words.Saving.ResourceSavingArgs klas. Stellt Daten für die bereitResourceSaving event in C#.
type: docs
weight: 5560
url: /de/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

Stellt Daten für die bereit[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) event.

Um mehr zu erfahren, besuchen Sie die[Speichern Sie ein Dokument](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

```csharp
public class ResourceSavingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | Ruft das Dokumentobjekt ab, das gerade gespeichert wird. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | Gibt an, ob Aspose.Words den Stream offen halten oder schließen soll, nachdem eine Ressource gespeichert wurde. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | Ruft den Dateinamen (ohne Pfad) ab, unter dem die Ressource gespeichert wird, oder legt diesen fest. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | Ruft den Uniform Resource Identifier (URI) ab, der zum Verweisen auf die Ressourcendatei aus dem Dokument verwendet wird, oder legt diesen fest. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | Ermöglicht die Angabe des Streams, in dem die Ressource gespeichert wird. |

## Bemerkungen

Wenn Aspose.Words ein Dokument im HTML- oder SVG-Format mit fester Seite speichert, speichert es standardmäßig jede Ressource in einer separaten Datei . Aspose.Words verwendet den Dateinamen des Dokuments und eine eindeutige Nummer, um für jede im Dokument gefundene Ressource einen eindeutigen Dateinamen zu generieren.

`ResourceSavingArgs` Ermöglicht die Neudefinition der Generierung von Ressourcendateinamen oder die vollständige Umgehung des Speicherns von Ressourcen in Dateien durch die Bereitstellung eigener Stream-Objekte.

Um Ihre eigene Logik zum Generieren von Ressourcendateinamen anzuwenden, verwenden Sie [`ResourceFileName`](./resourcefilename/) Eigentum.

Um Ressourcen in Streams statt in Dateien zu speichern, verwenden Sie die[`ResourceStream`](./resourcestream/) Eigentum.

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
