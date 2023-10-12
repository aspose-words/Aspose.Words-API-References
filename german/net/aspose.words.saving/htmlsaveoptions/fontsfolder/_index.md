---
title: HtmlSaveOptions.FontsFolder
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt den physischen Ordner an in dem Schriftarten gespeichert werden wenn ein Dokument nach HTML exportiert wird. Der Standardwert ist eine leere Zeichenfolge.
type: docs
weight: 310
url: /de/net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

Gibt den physischen Ordner an, in dem Schriftarten gespeichert werden, wenn ein Dokument nach HTML exportiert wird. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string FontsFolder { get; set; }
```

### Bemerkungen

Wenn Sie a speichern[`Document`](../../../aspose.words/document/) im HTML-Format und[`ExportFontResources`](../exportfontresources/) ist eingestellt auf`WAHR` , Aspose.Words muss die im Dokument verwendeten Schriftarten als eigenständige Dateien speichern. `FontsFolder` Hier können Sie angeben, wo die Schriftarten gespeichert werden und [`FontsFolderAlias`](../fontsfolderalias/) ermöglicht die Angabe, wie die Schriftart-URIs erstellt werden.

Wenn Sie ein Dokument in einer Datei speichern und einen Dateinamen angeben, speichert Aspose.Words die -Schriftarten standardmäßig im selben Ordner, in dem die Dokumentdatei gespeichert ist. Verwenden`FontsFolder` , um dieses Verhalten zu überschreiben.

Wenn Sie ein Dokument in einem Stream speichern, verfügt Aspose.Words über keinen Ordner zum Speichern der Schriftarten, , muss die Schriftarten jedoch trotzdem irgendwo speichern. In diesem Fall müssen Sie einen zugänglichen Ordner im angeben`FontsFolder` Eigenschaft oder stellen Sie benutzerdefinierte Streams über bereit[`FontSavingCallback`](../fontsavingcallback/) Ereignishandler.

Wenn der von angegebene Ordner`FontsFolder` nicht existiert, wird es automatisch erstellt.

[`ResourceFolder`](../resourcefolder/) ist eine weitere Möglichkeit, einen Ordner anzugeben, in dem Schriftarten gespeichert werden sollen.

### Beispiele

Zeigt, wie Ordner und Ordneraliase für extern gespeicherte Ressourcen festgelegt werden, die Aspose.Words beim Speichern eines Dokuments in HTML erstellt.

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
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


