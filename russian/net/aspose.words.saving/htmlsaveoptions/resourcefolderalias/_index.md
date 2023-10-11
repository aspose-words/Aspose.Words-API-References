---
title: HtmlSaveOptions.ResourceFolderAlias
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Указывает имя папки используемой для создания URI всех ресурсов записанных в HTMLдокумент. Значение по умолчанию  пустая строка.
type: docs
weight: 430
url: /ru/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

Указывает имя папки, используемой для создания URI всех ресурсов, записанных в HTML-документ. Значение по умолчанию — пустая строка.

```csharp
public string ResourceFolderAlias { get; set; }
```

### Примечания

`ResourceFolderAlias` это самый простой способ указать, как должны быть созданы URI для всех файлов ресурсов. Эту же информацию можно указать для изображений и шрифтов отдельно через[`ImagesFolderAlias`](../imagesfolderalias/) и[`FontsFolderAlias`](../fontsfolderalias/) свойства соответственно. Однако для CSS. нет отдельного свойства.

`ResourceFolderAlias` имеет более низкий приоритет, чем[`FontsFolderAlias`](../fontsfolderalias/) и[`ImagesFolderAlias`](../imagesfolderalias/) . Например, если оба`ResourceFolderAlias` и[`FontsFolderAlias`](../fontsfolderalias/) указаны, URI шрифтов будут созданы с использованием [`FontsFolderAlias`](../fontsfolderalias/) , а URI изображений и CSS будут созданы с использованием `ResourceFolderAlias`.

Если`ResourceFolderAlias` пусто,[`ResourceFolder`](../resourcefolder/)Значение свойства будет использоваться для создания URI ресурсов.

Если`ResourceFolderAlias` установлено значение '.' (точка), URI ресурсов будут содержать только имена файлов без какого-либо пути.

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
    FontsFolderAlias = "http://example.com/fonts",
    ImagesFolderAlias = "http://example.com/images",
    ResourceFolderAlias = "http://example.com/resources",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


