---
title: HtmlSaveOptions.FontsFolderAlias
linktitle: FontsFolderAlias
articleTitle: FontsFolderAlias
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HtmlSaveOptions FontsFolderAlias для настройки URI шрифтов в ваших HTML-документах. Улучшите свой веб-дизайн с легкостью!
type: docs
weight: 320
url: /ru/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

Указывает имя папки, используемой для создания URI шрифтов, записанных в HTML-документ. По умолчанию — пустая строка.

```csharp
public string FontsFolderAlias { get; set; }
```

## Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате HTML и[`ExportFontResources`](../exportfontresources/) установлен на`истинный` , Aspose.Words необходимо сохранять шрифты, используемые в документе, как отдельные файлы. [`FontsFolder`](../fontsfolder/) позволяет указать, где будут сохранены шрифты and `FontsFolderAlias` позволяет указать, как будут построены URI шрифтов.

Если`FontsFolderAlias` не пустая строка, то URI шрифтаwritten в HTML будетFontsFolderAlias + &lt;имя файла шрифта&gt;.

Если`FontsFolderAlias` пустая строка, то URI шрифтаwritten в HTML будетFontsFolder + &lt;имя файла шрифта&gt;.

Если`FontsFolderAlias`установлено значение «.» (точка), то имя файла шрифта будет записано в HTML без пути независимо от других параметров.

Альтернативный способ указать имя папки для построения шрифта URIs — использовать[`ResourceFolderAlias`](../resourcefolderalias/).

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
