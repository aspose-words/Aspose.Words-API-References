---
title: ImageSaveOptions.ImageColorMode
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImageSaveOptions ImageColorMode, чтобы легко настраивать и оптимизировать цветовой режим для ваших сгенерированных изображений. Улучшите свои визуальные эффекты сегодня!
type: docs
weight: 50
url: /ru/net/aspose.words.saving/imagesaveoptions/imagecolormode/
---
## ImageSaveOptions.ImageColorMode property

Получает или задает цветовой режим для созданных изображений.

```csharp
public ImageColorMode ImageColorMode { get; set; }
```

## Примечания

Это свойство действует только при сохранении в растровых форматах изображений.

Значение по умолчанию:None.

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

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
