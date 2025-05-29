---
title: HtmlSaveOptions.ResourceFolderAlias
linktitle: ResourceFolderAlias
articleTitle: ResourceFolderAlias
second_title: Aspose.Words для .NET
description: Оптимизируйте свои HTML-документы с помощью свойства HtmlSaveOptions ResourceFolderAlias, определяющего имена папок для эффективного построения URI ресурсов.
type: docs
weight: 450
url: /ru/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

Указывает имя папки, используемой для построения URI всех ресурсов, записанных в HTML-документ. По умолчанию — пустая строка.

```csharp
public string ResourceFolderAlias { get; set; }
```

## Примечания

`ResourceFolderAlias` это самый простой способ указать, как должны быть построены URI для всех файлов ресурсов . Та же информация может быть указана для изображений и шрифтов отдельно через[`ImagesFolderAlias`](../imagesfolderalias/) и[`FontsFolderAlias`](../fontsfolderalias/) свойства, соответственно. Однако, для CSS. нет отдельного свойства

`ResourceFolderAlias` имеет более низкий приоритет, чем[`FontsFolderAlias`](../fontsfolderalias/) и[`ImagesFolderAlias`](../imagesfolderalias/) . Например, если оба`ResourceFolderAlias` и[`FontsFolderAlias`](../fontsfolderalias/) указаны, URI шрифтов будут созданы с использованием [`FontsFolderAlias`](../fontsfolderalias/) тогда как URI изображений и CSS будут созданы с использованием `ResourceFolderAlias`.

Если`ResourceFolderAlias` пусто,[`ResourceFolder`](../resourcefolder/) Значение свойства будет использовано для построения URI ресурсов.

Если`ResourceFolderAlias` установлено значение «.» (точка), URI ресурсов будут содержать только имена файлов, без любого пути.

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
