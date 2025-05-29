---
title: HtmlSaveOptions.ResourceFolder
linktitle: ResourceFolder
articleTitle: ResourceFolder
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HtmlSaveOptions ResourceFolder для оптимального экспорта документов. Легко управляйте изображениями, шрифтами и CSS в назначенной папке.
type: docs
weight: 440
url: /ru/net/aspose.words.saving/htmlsaveoptions/resourcefolder/
---
## HtmlSaveOptions.ResourceFolder property

Указывает физическую папку, в которой сохраняются все ресурсы, такие как изображения, шрифты и внешний CSS, когда document экспортируется в HTML. По умолчанию — пустая строка.

```csharp
public string ResourceFolder { get; set; }
```

## Примечания

`ResourceFolder` это самый простой способ указать папку, в которую должны быть записаны все ресурсы. Другой способ — использовать отдельные свойства[`FontsFolder`](../fontsfolder/) ,[`ImagesFolder`](../imagesfolder/) , и[`CssStyleSheetFileName`](../cssstylesheetfilename/).

`ResourceFolder` имеет более низкий приоритет, чем папки, указанные через[`FontsFolder`](../fontsfolder/) , [`ImagesFolder`](../imagesfolder/) , и[`CssStyleSheetFileName`](../cssstylesheetfilename/) . Например, если both `ResourceFolder` и[`FontsFolder`](../fontsfolder/)указаны, шрифты будут сохранены в[`FontsFolder`](../fontsfolder/) , а изображения и CSS будут сохранены в`ResourceFolder`.

Если папка указана`ResourceFolder` не существует, он будет создан автоматически.

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
