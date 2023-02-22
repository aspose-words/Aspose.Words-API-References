---
title: HtmlSaveOptions.ImageResolution
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt die Ausgabeauflösung für Bilder beim Exportieren in HTML MHTML oder EPUB an. Standard ist96 dpi .
type: docs
weight: 350
url: /de/net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

Gibt die Ausgabeauflösung für Bilder beim Exportieren in HTML, MHTML oder EPUB an. Standard ist`96 dpi` .

```csharp
public int ImageResolution { get; set; }
```

### Bemerkungen

Diese Eigenschaft wirkt sich auf Rasterbilder aus, wenn[`ScaleImageToShapeSize`](../scaleimagetoshapesize/) ist`Stimmt` und Effekt-Metadateien, die als Rasterbilder exportiert werden. Einige Bildeigenschaften wie Zuschneiden oder Drehung erfordern das Speichern transformierter Bilder, und in diesem Fall werden transformierte Bilder in der gegebenen -Auflösung erstellt.

### Beispiele

Zeigt, wie Ordner und Ordneraliase für extern gespeicherte Ressourcen festgelegt werden, die Aspose.Words erstellt, wenn ein Dokument in HTML gespeichert wird.

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

* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


