---
title: HtmlSaveOptions.ImageResolution
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt die Ausgabeauflösung für Bilder beim Exportieren nach HTML MHTML oder EPUB an. Die Standardeinstellung ist96 dpi .
type: docs
weight: 340
url: /de/net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

Gibt die Ausgabeauflösung für Bilder beim Exportieren nach HTML, MHTML oder EPUB an. Die Standardeinstellung ist`96 dpi` .

```csharp
public int ImageResolution { get; set; }
```

### Bemerkungen

Diese Eigenschaft wirkt sich auf Rasterbilder aus, wenn[`ScaleImageToShapeSize`](../scaleimagetoshapesize/) ist`WAHR` und Effektmetadateien, die als Rasterbilder exportiert werden. Einige Bildeigenschaften wie Zuschneiden oder Drehung erfordern das Speichern transformierter Bilder. In diesem Fall werden transformierte Bilder in der angegebenen -Auflösung erstellt.

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

* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


