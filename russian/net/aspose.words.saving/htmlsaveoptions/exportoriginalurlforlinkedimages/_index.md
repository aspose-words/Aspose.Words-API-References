---
title: HtmlSaveOptions.ExportOriginalUrlForLinkedImages
linktitle: ExportOriginalUrlForLinkedImages
articleTitle: ExportOriginalUrlForLinkedImages
second_title: Aspose.Words для .NET
description: Откройте для себя функцию ExportOriginalUrlForLinkedImages от HtmlSaveOptions, позволяющую использовать оригинальные URL-адреса для связанных изображений. Повысьте целостность вашего документа!
type: docs
weight: 200
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions.ExportOriginalUrlForLinkedImages property

Указывает, следует ли использовать исходный URL-адрес в качестве URL-адреса связанных изображений. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportOriginalUrlForLinkedImages { get; set; }
```

## Примечания

Если установлено значение`истинный`[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) значение используется как URL-адрес связанных изображений, а связанные изображения не загружаются в папку документа или[`ImagesFolder`](../imagesfolder/).

Если установлено значение`ЛОЖЬ`связанные изображения загружаются в папку документа или[`ImagesFolder`](../imagesfolder/) и URL каждого связанного изображения формируется в зависимости от папки документа,[`ImagesFolder`](../imagesfolder/) и[`ImagesFolderAlias`](../imagesfolderalias/) характеристики.

## Примеры

Показывает, как задать папки и псевдонимы папок для внешних сохраненных ресурсов, которые Aspose.Words создаст при сохранении документа в формате HTML.

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

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
