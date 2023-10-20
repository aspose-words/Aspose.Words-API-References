---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words для .NET
description: HtmlSaveOptions ImagesFolderAlias свойство. Указывает имя папки используемой для создания URI изображений записанных в HTMLдокумент. По умолчанию  пустая строка на С#.
type: docs
weight: 370
url: /ru/net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

Указывает имя папки, используемой для создания URI изображений, записанных в HTML-документ. По умолчанию — пустая строка.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате HTML Aspose.Words необходимо сохранить все изображения , встроенные в документ, как отдельные файлы.[`ImagesFolder`](../imagesfolder/) позволяет указать, где будут сохраняться изображения и`ImagesFolderAlias` позволяет указать, как будут создаваться URI изображения.

Если`ImagesFolderAlias` не пустая строка, то URI изображения, записанный в HTML, будет иметь видImagesFolderAlias + &lt;имя файла изображения&gt;.

Если`ImagesFolderAlias` является пустой строкой, то URI изображения, записанный в HTML, будет иметь видImagesFolder + &lt;имя файла изображения&gt;.

Если`ImagesFolderAlias`установлено значение '.' (точка), то имя файла изображения будет записано в HTML без пути независимо от других параметров.

Альтернативный способ указать имя папки для создания URIs изображения — использовать[`ResourceFolderAlias`](../resourcefolderalias/).

## Примеры

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
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
