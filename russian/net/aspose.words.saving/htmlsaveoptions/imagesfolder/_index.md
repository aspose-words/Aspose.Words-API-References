---
title: HtmlSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HtmlSaveOptions ImagesFolder. Легко задайте папку для сохранения изображений при экспорте документов в HTML. Оптимизируйте свой рабочий процесс сегодня!
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

Когда вы сохраняете[`Document`](../../../aspose.words/document/) в формате HTML Aspose.Words необходимо сохранить все изображения, встроенные в документ, как отдельные файлы.`ImagesFolder` позволяет указать, где будут сохранены изображения и[`ImagesFolderAlias`](../imagesfolderalias/) позволяет указать, как будут формироваться URI изображений.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения the в той же папке, где сохранен файл документа. Используйте`ImagesFolder` для переопределения этого поведения.

Если вы сохраняете документ в поток, Aspose.Words не имеет папки, куда можно сохранять изображения, , но все равно должен сохранять изображения где-то. В этом случае вам нужно указать доступную папку в`ImagesFolder` свойство или предоставить пользовательские потоки via [`ImageSavingCallback`](../imagesavingcallback/) обработчик событий.

Если папка указана`ImagesFolder` не существует, он будет создан автоматически.

[`ResourceFolder`](../resourcefolder/) — это еще один способ указать папку, в которой следует сохранять изображения.

## Примеры

Показывает, как указать папку для хранения связанных изображений после сохранения в формате .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Установите параметр для экспорта полей формы как обычного текста вместо элементов ввода HTML.
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
