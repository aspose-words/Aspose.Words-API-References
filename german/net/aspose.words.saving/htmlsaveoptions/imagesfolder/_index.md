---
title: HtmlSaveOptions.ImagesFolder
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt den physischen Ordner an in dem Bilder gespeichert werden wenn ein Dokument in das HTMLFormat exportiert wird. Standard ist eine leere Zeichenfolge.
type: docs
weight: 370
url: /de/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

Gibt den physischen Ordner an, in dem Bilder gespeichert werden, wenn ein Dokument in das HTML-Format exportiert wird. Standard ist eine leere Zeichenfolge.

```csharp
public string ImagesFolder { get; set; }
```

### Bemerkungen

Beim Speichern von a[`Document`](../../../aspose.words/document/) im HTML-Format muss Aspose.Words alle in das Dokument eingebetteten -Bilder als eigenständige Dateien speichern.`ImagesFolder` Mit können Sie angeben, wo die Bilder gespeichert werden und[`ImagesFolderAlias`](../imagesfolderalias/) ermöglicht die Angabe, wie die Bild-URIs aufgebaut werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words die -Bilder standardmäßig in demselben Ordner, in dem die Dokumentdatei gespeichert ist. Verwenden`ImagesFolder` , um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einem Stream speichern, hat Aspose.Words keinen Ordner zum Speichern der Bilder, muss die Bilder aber trotzdem irgendwo speichern. In diesem Fall müssen Sie einen zugänglichen Ordner in der angeben`ImagesFolder` Eigenschaft oder benutzerdefinierte Streams über bereitstellen[`ImageSavingCallback`](../imagesavingcallback/) Ereignishandler.

Wenn der angegebene Ordner durch`ImagesFolder` nicht existiert, wird sie automatisch erstellt.

[`ResourceFolder`](../resourcefolder/) ist eine weitere Möglichkeit, einen Ordner anzugeben, in dem Bilder gespeichert werden sollen.

### Beispiele

Zeigt, wie der Ordner zum Speichern verknüpfter Bilder nach dem Speichern in .html angegeben wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Legen Sie eine Option zum Exportieren von Formularfeldern als einfachen Text anstelle von HTML-Eingabeelementen fest.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


