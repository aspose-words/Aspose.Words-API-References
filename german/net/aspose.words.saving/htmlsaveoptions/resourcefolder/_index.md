---
title: HtmlSaveOptions.ResourceFolder
linktitle: ResourceFolder
articleTitle: ResourceFolder
second_title: Aspose.Words für .NET
description: Entdecken Sie die ResourceFolder-Eigenschaft HtmlSaveOptions für optimalen Dokumentexport. Verwalten Sie Bilder, Schriftarten und CSS ganz einfach in einem dafür vorgesehenen Ordner.
type: docs
weight: 440
url: /de/net/aspose.words.saving/htmlsaveoptions/resourcefolder/
---
## HtmlSaveOptions.ResourceFolder property

Gibt einen physischen Ordner an, in dem alle Ressourcen wie Bilder, Schriftarten und externes CSS gespeichert werden, wenn ein Dokument nach HTML exportiert wird. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string ResourceFolder { get; set; }
```

## Bemerkungen

`ResourceFolder` ist die einfachste Möglichkeit, einen Ordner anzugeben, in den alle Ressourcen geschrieben werden sollen. Eine andere Möglichkeit besteht darin, einzelne Eigenschaften zu verwenden[`FontsFolder`](../fontsfolder/) ,[`ImagesFolder`](../imagesfolder/) , und[`CssStyleSheetFileName`](../cssstylesheetfilename/).

`ResourceFolder` hat eine niedrigere Priorität als Ordner, die über[`FontsFolder`](../fontsfolder/) , [`ImagesFolder`](../imagesfolder/) , Und[`CssStyleSheetFileName`](../cssstylesheetfilename/) . Wenn beispielsweise both `ResourceFolder` Und[`FontsFolder`](../fontsfolder/)angegeben sind, werden Schriftarten gespeichert in[`FontsFolder`](../fontsfolder/) , während Bilder und CSS gespeichert werden unter`ResourceFolder`.

Wenn der von angegebene Ordner`ResourceFolder` nicht existiert, wird es automatisch erstellt.

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
