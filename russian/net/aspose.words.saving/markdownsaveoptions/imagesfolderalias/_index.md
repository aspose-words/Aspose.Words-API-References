---
title: MarkdownSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words для .NET
description: MarkdownSaveOptions ImagesFolderAlias свойство. Указывает имя папки используемой для создания URI изображений записываемых в документ. По умолчанию  пустая строка на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Указывает имя папки, используемой для создания URI изображений, записываемых в документ. По умолчанию — пустая строка.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) вMarkdown format, Aspose.Words необходимо сохранить все изображения, встроенные в документ, как отдельные файлы. [`ImagesFolder`](../imagesfolder/) позволяет указать, где будут сохраняться изображения and `ImagesFolderAlias` позволяет указать, как будут создаваться URI изображения.

Если`ImagesFolderAlias` не пустая строка, то URI изображения, записанный в Markdown, будет иметь видImagesFolderAlias + &lt;имя файла изображения&gt;.

Если`ImagesFolderAlias` является пустой строкой, то URI изображения, записанный в Markdown, будет иметь видImagesFolder + &lt;имя файла изображения&gt;.

Если`ImagesFolderAlias`установлено значение '.' (точка), то файл изображения name будет записан в Markdown без пути независимо от других параметров.

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
