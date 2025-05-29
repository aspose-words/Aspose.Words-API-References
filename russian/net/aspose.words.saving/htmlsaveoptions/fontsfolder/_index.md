---
title: HtmlSaveOptions.FontsFolder
linktitle: FontsFolder
articleTitle: FontsFolder
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HtmlSaveOptions FontsFolder, позволяющее легко управлять хранилищем шрифтов для экспорта в HTML, улучшая представление и доступность документов.
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

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате HTML и[`ExportFontResources`](../exportfontresources/) установлен на`истинный` , Aspose.Words необходимо сохранять шрифты, используемые в документе, как отдельные файлы. `FontsFolder` позволяет указать, где будут сохранены шрифты and [`FontsFolderAlias`](../fontsfolderalias/) позволяет указать, как будут построены URI шрифтов.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет шрифты the в той же папке, где сохранен файл документа. Используйте`FontsFolder` для переопределения этого поведения.

Если вы сохраняете документ в поток, Aspose.Words не имеет папки, куда сохранять шрифты, , но все равно должен где-то сохранять шрифты. В этом случае вам нужно указать доступную папку в`FontsFolder` свойство или предоставить пользовательские потоки via [`FontSavingCallback`](../fontsavingcallback/) обработчик событий.

Если папка указана`FontsFolder` не существует, он будет создан автоматически.

[`ResourceFolder`](../resourcefolder/) — это еще один способ указать папку, в которой следует сохранять шрифты.

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
