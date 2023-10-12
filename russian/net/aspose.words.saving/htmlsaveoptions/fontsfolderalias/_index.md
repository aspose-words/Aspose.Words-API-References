---
title: HtmlSaveOptions.FontsFolderAlias
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Указывает имя папки используемой для создания URI шрифтов записанных в HTMLдокумент. По умолчанию  пустая строка.
type: docs
weight: 320
url: /ru/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

Указывает имя папки, используемой для создания URI шрифтов, записанных в HTML-документ. По умолчанию — пустая строка.

```csharp
public string FontsFolderAlias { get; set; }
```

### Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате HTML и[`ExportFontResources`](../exportfontresources/) установлено на`истинный` , Aspose.Words необходимо сохранять шрифты, используемые в документе, как отдельные файлы. [`FontsFolder`](../fontsfolder/) позволяет указать, где будут сохраняться шрифты и `FontsFolderAlias` позволяет указать, как будут создаваться URI шрифтов.

Если`FontsFolderAlias` не пустая строка, то URI шрифта, записанный в HTML, будет иметь видFontsFolderAlias + &lt;имя файла шрифта&gt;.

Если`FontsFolderAlias` является пустой строкой, то URI шрифта, записанный в HTML, будет иметь видFontsFolder + &lt;имя файла шрифта&gt;.

Если`FontsFolderAlias`установлено значение '.' (точка), то имя файла шрифта будет записано в HTML без пути независимо от других параметров.

Альтернативный способ указать имя папки для создания URI шрифта — использовать[`ResourceFolderAlias`](../resourcefolderalias/).

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


