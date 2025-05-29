---
title: MarkdownSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words для .NET
description: Узнайте, как свойство MarkdownSaveOptions ImagesFolder улучшает экспорт документов, указывая идеальную папку для сохранения изображений в формате Markdown.
type: docs
weight: 80
url: /ru/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Указывает физическую папку, в которой сохраняются изображения при экспорте документа в Markdown формат. По умолчанию пустая строка.

```csharp
public string ImagesFolder { get; set; }
```

## Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) вMarkdownформат, Aspose.Words необходимо сохранить все изображения, встроенные в документ, как отдельные файлы. `ImagesFolder` позволяет указать, где будут сохранены изображения.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохранен файл документа. Используйте`ImagesFolder` чтобы переопределить это поведение.

Если вы сохраняете документ в поток, Aspose.Words не имеет папки , где можно сохранять изображения, но все равно должен сохранять изображения где-то. В этом случае вам нужно указать доступную папку в`ImagesFolder` свойство.

Если папка указана`ImagesFolder` не существует, он будет создан автоматически.

## Примеры

Показывает, как указать имя папки, используемой для создания URI изображений.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
builder.InsertImage(ImageDir + "Logo.jpg");

string imagesFolder = Path.Combine(ArtifactsDir, "ImagesDir");
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Используйте свойство "ImagesFolder", чтобы назначить папку в локальной файловой системе, в которую
// Aspose.Words сохранит все связанные изображения документа.
saveOptions.ImagesFolder = imagesFolder;
// Используйте свойство "ImagesFolderAlias" для использования этой папки
// при построении URI изображений вместо имени папки с изображениями.
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### Смотрите также

* class [MarkdownSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
