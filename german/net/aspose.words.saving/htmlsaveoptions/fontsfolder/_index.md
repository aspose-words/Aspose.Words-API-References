---
title: HtmlSaveOptions.FontsFolder
linktitle: FontsFolder
articleTitle: FontsFolder
second_title: Aspose.Words für .NET
description: Entdecken Sie die FontsFolder-Eigenschaft von HtmlSaveOptions, um die Schriftartenspeicherung für HTML-Exporte einfach zu verwalten und so die Dokumentpräsentation und -zugänglichkeit zu verbessern.
type: docs
weight: 310
url: /de/net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

Gibt den physischen Ordner an, in dem Schriftarten beim Exportieren eines Dokuments nach HTML gespeichert werden. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string FontsFolder { get; set; }
```

## Bemerkungen

Wenn Sie eine[`Document`](../../../aspose.words/document/) im HTML-Format und[`ExportFontResources`](../exportfontresources/) ist eingestellt auf`WAHR` , Aspose.Words muss die im Dokument verwendeten Schriftarten als eigenständige Dateien speichern. `FontsFolder` ermöglicht Ihnen, anzugeben, wo die Schriftarten gespeichert werden und [`FontsFolderAlias`](../fontsfolderalias/) ermöglicht die Angabe, wie die Schriftart-URIs erstellt werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words standardmäßig die Schriftarten im selben Ordner wie die Dokumentdatei. Verwenden Sie`FontsFolder` , um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einem Stream speichern, verfügt Aspose.Words nicht über einen Ordner, in dem die Schriftarten gespeichert werden können, , muss die Schriftarten aber trotzdem irgendwo speichern. In diesem Fall müssen Sie einen zugänglichen Ordner in der`FontsFolder` Eigenschaft oder stellen Sie benutzerdefinierte Streams bereit via die[`FontSavingCallback`](../fontsavingcallback/) Ereignishandler.

Wenn der von angegebene Ordner`FontsFolder` nicht vorhanden ist, wird es automatisch erstellt.

[`ResourceFolder`](../resourcefolder/) ist eine weitere Möglichkeit, einen Ordner anzugeben, in dem Schriftarten gespeichert werden sollen.

## Beispiele

Zeigt, wie Ordner und Ordneraliase für extern gespeicherte Ressourcen festgelegt werden, die Aspose.Words beim Speichern eines Dokuments im HTML-Format erstellt.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    ImageResolution = 72,
    FontResourcesSubsettingSizeThreshold = 0,
    FontsFolder = ArtifactsDir + "Fonts",
    ImagesFolder = ArtifactsDir + "Images",
    ResourceFolder = ArtifactsDir + "Resources",
    FontsFolderAlias = "http://example.com/fonts",
    ImagesFolderAlias = "http://example.com/images",
    ResourceFolderAlias = "http://example.com/resources",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
