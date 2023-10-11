---
title: ImageSaveOptions.ImageColorMode
second_title: Справочник по API Aspose.Words для .NET
description: ImageSaveOptions свойство. Получает или задает цветовой режим для создаваемых изображений.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/imagesaveoptions/imagecolormode/
---
## ImageSaveOptions.ImageColorMode property

Получает или задает цветовой режим для создаваемых изображений.

```csharp
public ImageColorMode ImageColorMode { get; set; }
```

### Примечания

Это свойство действует только при сохранении в форматах растровых изображений.

Значение по умолчанию:None.

### Примеры

Показывает, как установить цветовой режим при рендеринге документов.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // Когда мы сохраняем документ как изображение, мы можем передать объект SaveOptions
            // выбираем цветовой режим для изображения, которое будет создано при сохранении.
            // Если мы установим для свойства «ImageColorMode» значение «ImageColorMode.BlackAndWhite»,
            // операция сохранения будет применять уменьшение цвета в оттенках серого при рендеринге документа.
            // Если мы установим для свойства «ImageColorMode» значение «ImageColorMode.Grayscale»,
            // операция сохранения преобразует документ в монохромное изображение.
            // Если мы установим для свойства «ImageColorMode» значение «Нет», операция сохранения будет применять метод по умолчанию
            // и сохраним все цвета документа в выходном изображении.
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.ImageColorMode = imageColorMode;

            doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);

#if NET48 || JAVA
            switch (imageColorMode)
            {
                case ImageColorMode.None:
                    Assert.That(150000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.Grayscale:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.BlackAndWhite:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
            }
#elif NET5_0_OR_GREATER
            switch (imageColorMode)
            {
                case ImageColorMode.None:
                    Assert.That(120000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.Grayscale:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.BlackAndWhite:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
            }
#endif
```

### Смотрите также

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../imagesaveoptions/)
* сборка [Aspose.Words](../../../)


