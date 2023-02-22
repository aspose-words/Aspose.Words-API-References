---
title: MarkdownSaveOptions.ImagesFolder
second_title: Справочник по API Aspose.Words для .NET
description: MarkdownSaveOptions свойство. Указывает физическую папку в которой сохраняются изображения при экспорте документа в Markdown формат. По умолчанию это пустая строка.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Указывает физическую папку, в которой сохраняются изображения при экспорте документа в Markdown формат. По умолчанию это пустая строка.

```csharp
public string ImagesFolder { get; set; }
```

### Примечания

При сохранении[`Document`](../../../aspose.words/document/) вMarkdown формат, Aspose.Words необходимо сохранить все изображения, встроенные в документ, как отдельные файлы. `ImagesFolder` позволяет указать, где будут сохраняться изображения.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохранен файл документа. Использовать`ImagesFolder` переопределить это поведение.

Если вы сохраняете документ в поток, Aspose.Words не имеет папки , где можно сохранить изображения, но все равно нужно куда-то сохранять изображения. В этом случае нужно указать доступную папку в`ImagesFolder` свойство.

Если папка, указанная`ImagesFolder` не существует, он будет создан автоматически.

### Смотрите также

* class [MarkdownSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../markdownsaveoptions/)
* сборка [Aspose.Words](../../../)


