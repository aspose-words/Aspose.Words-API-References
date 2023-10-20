---
title: HtmlSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words для .NET
description: HtmlSaveOptions ImagesFolder свойство. Указывает физическую папку в которой сохраняются изображения при экспорте документа в формат HTML. По умолчанию  пустая строка на С#.
type: docs
weight: 360
url: /ru/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат HTML. По умолчанию — пустая строка.

```csharp
public string ImagesFolder { get; set; }
```

## Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате HTML Aspose.Words необходимо сохранить все изображения , встроенные в документ, как отдельные файлы.`ImagesFolder` позволяет указать, где будут сохраняться изображения и[`ImagesFolderAlias`](../imagesfolderalias/) позволяет указать, как будут создаваться URI изображения.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохраняется файл документа. Использовать`ImagesFolder` , чтобы переопределить это поведение.

Если вы сохраняете документ в поток, Aspose.Words не имеет папки для сохранения изображений , но все равно необходимо где-то сохранять изображения. В этом случае вам необходимо указать доступную папку в`ImagesFolder` или предоставить собственные потоки через [`ImageSavingCallback`](../imagesavingcallback/) обработчик события.

Если папка, указанная`ImagesFolder` не существует, он будет создан автоматически.

[`ResourceFolder`](../resourcefolder/) это еще один способ указать папку, в которой следует сохранять изображения.

## Примеры

Показывает, как указать папку для хранения связанных изображений после сохранения в .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Установите опцию для экспорта полей формы в виде обычного текста вместо элементов ввода HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
