---
title: HtmlSaveOptions.ScaleImageToShapeSize
linktitle: ScaleImageToShapeSize
articleTitle: ScaleImageToShapeSize
second_title: Aspose.Words для .NET
description: HtmlSaveOptions ScaleImageToShapeSize свойство. Указывает масштабируются ли изображения с помощью Aspose.Words до размера ограничивающей фигуры при экспорте в HTML MHTML или EPUB. Значение по умолчаниюистинный  на С#.
type: docs
weight: 450
url: /ru/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Указывает, масштабируются ли изображения с помощью Aspose.Words до размера ограничивающей фигуры при экспорте в HTML, MHTML или EPUB. Значение по умолчанию:`истинный` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

## Примечания

Изображение в документе Microsoft Word — это фигура. Форма имеет размер, а image имеет свой собственный размер. Размеры напрямую не связаны. Например, изображение может иметь размер 1024x786 пикселей, , но форма, отображающая это изображение, может иметь размер 400x300 точек.

Чтобы отобразить изображение в браузере, его необходимо масштабировать до размера фигуры. `ScaleImageToShapeSize` элементы управления свойствами, где происходит масштабирование image : в Aspose.Words при экспорте в HTML или в браузере при отображении документа.

Когда`ScaleImageToShapeSize` является`истинный` , изображение масштабируется Aspose.Words с использованием высококачественного масштабирования во время экспорта в HTML. Когда`ScaleImageToShapeSize` это`ЛОЖЬ`, изображение выводится в исходном размере, и браузеру приходится его масштабировать.

В целом браузеры масштабируют быстро и некачественно. В результате вы обычно получаете лучшее качество отображения в браузере и меньший размер файла при`ScaleImageToShapeSize` является`истинный` , , но лучшее качество печати и более быстрое преобразование, когда`ScaleImageToShapeSize` является`ЛОЖЬ`.

Помимо фигур, содержащих отдельные растровые изображения, этот параметр также влияет на групповые фигуры, состоящие из растровых изображений. Если`ScaleImageToShapeSize` является`ЛОЖЬ` а фигура группы содержит растровые изображения , собственное разрешение которых выше значения, указанного в[`ImageResolution`](../imageresolution/), Aspose.Words will увеличит разрешение рендеринга для этой группы. Это позволяет лучше сохранить качество сгруппированных изображений высокого разрешения при сохранении в HTML.

## Примеры

Показывает, как отключить масштабирование изображений до размеров родительской фигуры при сохранении в формате .html.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Вставляем фигуру, содержащую изображение, а затем делаем эту фигуру значительно меньше изображения.
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            Shape imageShape = builder.InsertImage(image);
            imageShape.Width = 50;
            imageShape.Height = 50;

            // При сохранении документа, содержащего фигуры с изображениями, в HTML будет создан файл изображения в локальной файловой системе.
            // для каждой такой фигуры. Выходной HTML-документ будет использовать <image> теги для ссылки и отображения этих изображений.
            // Когда мы сохраняем документ в HTML, мы можем передать объект SaveOptions, чтобы определить
            // нужно ли масштабировать все изображения, находящиеся внутри фигур, до размеров их фигур.
            // Установка флага "ScaleImageToShapeSize" в значение "true" приведет к уменьшению каждого изображения
            // к размеру фигуры, которая его содержит, чтобы никакие сохраненные изображения не были больше, чем требует документ.
            // Установка флага ScaleImageToShapeSize в значение «false» сохранит исходные размеры этих изображений,
            // который займет больше места в обмен на сохранение качества изображения.
            HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

            doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);

            FileInfo fileInfo = new FileInfo(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.001.png");

#if NET48 || JAVA
        if (scaleImageToShapeSize)
            Assert.That(3000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(20000, Is.LessThan(fileInfo.Length));
#elif NET5_0_OR_GREATER
        if (scaleImageToShapeSize)
            Assert.That(10000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(30000, Is.LessThan(fileInfo.Length));
#endif
```

### Смотрите также

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
