---
title: HtmlSaveOptions.ExportOriginalUrlForLinkedImages
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt an ob die OriginalURL als URL der verknüpften Bilder verwendet werden soll. Der Standardwert istFALSCH .
type: docs
weight: 200
url: /de/net/aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions.ExportOriginalUrlForLinkedImages property

Gibt an, ob die Original-URL als URL der verknüpften Bilder verwendet werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool ExportOriginalUrlForLinkedImages { get; set; }
```

### Bemerkungen

Wenn der Wert auf eingestellt ist`WAHR`[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) Der Wert wird verwendet , da die URL verknüpfter Bilder und verknüpfte Bilder nicht in den Ordner des Dokuments geladen werden oder[`ImagesFolder`](../imagesfolder/).

Wenn der Wert auf eingestellt ist`FALSCH`Verlinkte Bilder werden in den Ordner des Dokuments geladen[`ImagesFolder`](../imagesfolder/) und die URL jedes verknüpften Bildes wird abhängig vom Ordner des Dokuments erstellt.[`ImagesFolder`](../imagesfolder/) und[`ImagesFolderAlias`](../imagesfolderalias/) Eigenschaften.

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


