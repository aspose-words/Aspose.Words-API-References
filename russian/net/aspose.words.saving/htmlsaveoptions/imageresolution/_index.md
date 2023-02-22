---
title: HtmlSaveOptions.ImageResolution
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Определяет выходное разрешение для изображений при экспорте в HTML MHTML или EPUB. Значение по умолчанию96 точек на дюйм .
type: docs
weight: 350
url: /ru/net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

Определяет выходное разрешение для изображений при экспорте в HTML, MHTML или EPUB. Значение по умолчанию:`96 точек на дюйм` .

```csharp
public int ImageResolution { get; set; }
```

### Примечания

Это свойство влияет на растровые изображения, когда[`ScaleImageToShapeSize`](../scaleimagetoshapesize/) это`истинный` метафайлы эффектов экспортируются как растровые изображения. Некоторые свойства изображения, такие как обрезка или поворот, требуют сохранения преобразованных изображений, и в этом случае преобразованные изображения создаются с разрешением заданное .

### Примеры

Показывает, как установить папки и псевдонимы папок для внешне сохраненных ресурсов, которые Aspose.Words создаст при сохранении документа в HTML.

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
    FontsFolderAlias = "http://example.com/шрифты",
    ImagesFolderAlias = "http://example.com/images",
    ResourceFolderAlias = "http://example.com/resources",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Смотрите также

* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


