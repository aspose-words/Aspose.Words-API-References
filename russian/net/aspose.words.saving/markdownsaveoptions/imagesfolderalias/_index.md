---
title: MarkdownSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MarkdownSaveOptions ImagesFolderAlias, чтобы легко управлять URI изображений в ваших документах. Оптимизируйте свой рабочий процесс с помощью этой важной функции!
type: docs
weight: 90
url: /ru/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Указывает имя папки, используемой для создания URI изображений, записанных в документ. По умолчанию — пустая строка.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Примечания

Когда вы сохраняете[`Document`](../../../aspose.words/document/) вMarkdown формат, Aspose.Words необходимо сохранить все изображения, встроенные в документ, как отдельные файлы. [`ImagesFolder`](../imagesfolder/) позволяет указать, где будут сохранены изображения and `ImagesFolderAlias` позволяет указать, как будут формироваться URI изображений.

Если`ImagesFolderAlias` не пустая строка, то URI изображенияwritten в Markdown будетImagesFolderAlias + &lt;имя файла изображения&gt;.

Если`ImagesFolderAlias` пустая строка, то URI изображенияwritten в Markdown будетImagesFolder + &lt;имя файла изображения&gt;.

Если`ImagesFolderAlias` установлено значение «.» (точка), то имя файла изображения будет записано в Markdown без пути независимо от других параметров.

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
