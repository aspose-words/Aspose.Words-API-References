---
title: HtmlSaveOptions.ExportOriginalUrlForLinkedImages
linktitle: ExportOriginalUrlForLinkedImages
articleTitle: ExportOriginalUrlForLinkedImages
second_title: Aspose.Words für .NET
description: Entdecken Sie die Funktion „ExportOriginalUrlForLinkedImages“ von HtmlSaveOptions, mit der Sie Original-URLs für verknüpfte Bilder verwenden können. Verbessern Sie die Integrität Ihres Dokuments!
type: docs
weight: 200
url: /de/net/aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions.ExportOriginalUrlForLinkedImages property

Gibt an, ob die ursprüngliche URL als URL der verknüpften Bilder verwendet werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool ExportOriginalUrlForLinkedImages { get; set; }
```

## Bemerkungen

Wenn der Wert auf`WAHR`[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) Der Wert wird als URL der verknüpften Bilder verwendet und die verknüpften Bilder werden nicht in den Ordner des Dokuments geladen oder[`ImagesFolder`](../imagesfolder/).

Wenn der Wert auf`FALSCH`Verknüpfte Bilder werden in den Ordner des Dokuments geladen oder[`ImagesFolder`](../imagesfolder/) und die URL jedes verknüpften Bildes wird abhängig vom Ordner des Dokuments erstellt,[`ImagesFolder`](../imagesfolder/) und[`ImagesFolderAlias`](../imagesfolderalias/) Eigenschaften.

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
