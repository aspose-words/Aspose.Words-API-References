---
title: HtmlSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words für .NET
description: Entdecken Sie die HtmlSaveOptions ImagesFolder-Eigenschaft. Legen Sie beim Exportieren von Dokumenten in HTML ganz einfach den Ordner für die Bildspeicherung fest. Optimieren Sie Ihren Workflow noch heute!
type: docs
weight: 360
url: /de/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

Gibt den physischen Ordner an, in dem Bilder beim Exportieren eines Dokuments in das HTML-Format gespeichert werden. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string ImagesFolder { get; set; }
```

## Bemerkungen

Wenn Sie eine[`Document`](../../../aspose.words/document/) Im HTML-Format muss Aspose.Words alle im Dokument eingebetteten -Bilder als eigenständige Dateien speichern.`ImagesFolder` ermöglicht Ihnen, festzulegen, wo die Bilder gespeichert werden und[`ImagesFolderAlias`](../imagesfolderalias/) ermöglicht die Angabe, wie die Bild-URIs erstellt werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words die -Bilder standardmäßig im selben Ordner wie die Dokumentdatei. Verwenden Sie`ImagesFolder` , um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einem Stream speichern, verfügt Aspose.Words nicht über einen Ordner, in dem die Bilder gespeichert werden können, , muss die Bilder aber trotzdem irgendwo speichern. In diesem Fall müssen Sie einen zugänglichen Ordner in der`ImagesFolder` Eigenschaft oder stellen Sie benutzerdefinierte Streams bereit via die[`ImageSavingCallback`](../imagesavingcallback/) Ereignishandler.

Wenn der von angegebene Ordner`ImagesFolder` nicht vorhanden ist, wird es automatisch erstellt.

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
