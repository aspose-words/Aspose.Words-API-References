---
title: ImageColorMode Enum
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Saving.ImageColorMode для оптимизации изображений страниц документов. Управляйте цветовыми режимами для улучшения визуального качества в ваших проектах.
type: docs
weight: 5960
url: /ru/net/aspose.words.saving/imagecolormode/
---
## ImageColorMode enumeration

Задает цветовой режим для создаваемых изображений страниц документа.

```csharp
public enum ImageColorMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Страницы документа будут отображаться как цветные изображения. |
| Grayscale | `1` | Страницы документа будут отображаться как изображения в оттенках серого. |
| BlackAndWhite | `2` | Страницы документа будут отображаться как черно-белые изображения. |

## Примеры

Показывает, как установить цветовой режим при рендеринге документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Когда мы сохраняем документ как изображение, мы можем передать объект SaveOptions
// выберите цветовой режим для изображения, которое будет создано при операции сохранения.
// Если мы установим свойство "ImageColorMode" на "ImageColorMode.BlackAndWhite",
// операция сохранения применит уменьшение оттенков серого при рендеринге документа.
 // Если мы установим свойство "ImageColorMode" на "ImageColorMode.Grayscale",
// операция сохранения преобразует документ в монохромное изображение.
// Если мы установим свойство "ImageColorMode" на "None", операция сохранения будет применять метод по умолчанию
// и сохранить все цвета документа в выходном изображении.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.ImageColorMode = imageColorMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
