---
title: HtmlSaveOptions.FontsFolder
linktitle: FontsFolder
articleTitle: FontsFolder
second_title: Aspose.Words для .NET
description: HtmlSaveOptions FontsFolder свойство. Указывает физическую папку в которой сохраняются шрифты при экспорте документа в HTML. По умолчанию  пустая строка на С#.
type: docs
weight: 310
url: /ru/net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

Указывает физическую папку, в которой сохраняются шрифты при экспорте документа в HTML. По умолчанию — пустая строка.

```csharp
public string FontsFolder { get; set; }
```

## Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате HTML и[`ExportFontResources`](../exportfontresources/) установлено на`истинный` , Aspose.Words необходимо сохранять шрифты, используемые в документе, как отдельные файлы. `FontsFolder` позволяет указать, где будут сохраняться шрифты и [`FontsFolderAlias`](../fontsfolderalias/) позволяет указать, как будут создаваться URI шрифтов.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет шрифты в той же папке, где сохраняется файл документа. Использовать`FontsFolder` , чтобы переопределить это поведение.

Если вы сохраняете документ в поток, Aspose.Words не имеет папки для сохранения шрифтов , но шрифты все равно нужно куда-то сохранять. В этом случае вам необходимо указать доступную папку в`FontsFolder` или предоставить собственные потоки через [`FontSavingCallback`](../fontsavingcallback/) обработчик события.

Если папка, указанная`FontsFolder` не существует, он будет создан автоматически.

[`ResourceFolder`](../resourcefolder/) это еще один способ указать папку, в которой следует сохранять шрифты.

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
