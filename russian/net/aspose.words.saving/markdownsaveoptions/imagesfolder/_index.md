---
title: MarkdownSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words для .NET
description: MarkdownSaveOptions ImagesFolder свойство. Указывает физическую папку в которой сохраняются изображения при экспорте документа в Markdown формат. По умолчанию  пустая строка на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Указывает физическую папку, в которой сохраняются изображения при экспорте документа в Markdown формат. По умолчанию — пустая строка.

```csharp
public string ImagesFolder { get; set; }
```

## Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) вMarkdownformat, Aspose.Words необходимо сохранить все изображения, встроенные в документ, как отдельные файлы. `ImagesFolder` позволяет указать, где будут сохраняться изображения.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в в той же папке, где сохраняется файл документа. Использовать`ImagesFolder` чтобы переопределить это поведение.

Если вы сохраняете документ в поток, Aspose.Words не имеет папки для сохранения изображений, но все равно необходимо где-то сохранять изображения. В этом случае необходимо указать доступную папку в`ImagesFolder` свойство.

Если папка, указанная`ImagesFolder` не существует, он будет создан автоматически.

## Примеры

Показывает, как указать имя папки, используемой для создания URI изображений.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
Image image = Image.FromFile(ImageDir + "Logo.jpg");
builder.InsertImage(image);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Используйте свойство «ImagesFolder», чтобы назначить папку в локальной файловой системе, в которую
// Aspose.Words сохранит все связанные изображения документа.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// Используйте свойство «ImagesFolderAlias» для использования этой папки
// при создании URI изображений вместо имени папки изображений.
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

Показывает, как указать имя папки, используемой для создания URI изображений (.NetStandard 2.0).

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(bitmap);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Используйте свойство «ImagesFolder», чтобы назначить папку в локальной файловой системе, в которую
// Aspose.Words сохранит все связанные изображения документа.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// Используйте свойство «ImagesFolderAlias» для использования этой папки
// при создании URI изображений вместо имени папки изображений.
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### Смотрите также

* class [MarkdownSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
