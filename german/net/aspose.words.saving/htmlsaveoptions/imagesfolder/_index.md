---
title: HtmlSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words für .NET
description: HtmlSaveOptions ImagesFolder eigendom. Gibt den physischen Ordner an in dem Bilder gespeichert werden wenn ein Dokument in das HTMLFormat exportiert wird. Der Standardwert ist eine leere Zeichenfolge in C#.
type: docs
weight: 360
url: /de/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

Gibt den physischen Ordner an, in dem Bilder gespeichert werden, wenn ein Dokument in das HTML-Format exportiert wird. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string ImagesFolder { get; set; }
```

## Bemerkungen

Wenn Sie a speichern[`Document`](../../../aspose.words/document/) Im HTML-Format muss Aspose.Words alle im Dokument eingebetteten -Bilder als eigenständige Dateien speichern.`ImagesFolder` Mit können Sie angeben, wo die Bilder gespeichert werden[`ImagesFolderAlias`](../imagesfolderalias/) ermöglicht die Angabe, wie die Bild-URIs erstellt werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words die -Bilder standardmäßig im selben Ordner, in dem die Dokumentdatei gespeichert ist. Verwenden`ImagesFolder` , um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einem Stream speichern, verfügt Aspose.Words über keinen Ordner zum Speichern der Bilder, , muss die Bilder aber trotzdem irgendwo speichern. In diesem Fall müssen Sie einen zugänglichen Ordner im angeben`ImagesFolder` Eigenschaft oder stellen Sie benutzerdefinierte Streams über bereit[`ImageSavingCallback`](../imagesavingcallback/) Ereignishandler.

Wenn der von angegebene Ordner`ImagesFolder` nicht existiert, wird es automatisch erstellt.

[`ResourceFolder`](../resourcefolder/) ist eine weitere Möglichkeit, einen Ordner anzugeben, in dem Bilder gespeichert werden sollen.

## Beispiele

Zeigt, wie der Ordner zum Speichern verknüpfter Bilder nach dem Speichern im HTML-Format angegeben wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Legen Sie eine Option fest, um Formularfelder als einfachen Text statt als HTML-Eingabeelemente zu exportieren.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
