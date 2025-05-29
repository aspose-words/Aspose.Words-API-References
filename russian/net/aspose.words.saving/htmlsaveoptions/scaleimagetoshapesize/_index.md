---
title: HtmlSaveOptions.ScaleImageToShapeSize
linktitle: ScaleImageToShapeSize
articleTitle: ScaleImageToShapeSize
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ScaleImageToShapeSize HtmlSaveOptions оптимизирует масштабирование изображения в Aspose.Words для экспорта HTML, MHTML или EPUB. Улучшите свои документы!
type: docs
weight: 470
url: /ru/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Указывает, масштабируются ли изображения Aspose.Words до размера ограничивающей фигуры при экспорте в HTML, MHTML или EPUB. Значение по умолчанию:`истинный` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

## Примечания

Изображение в документе Microsoft Word — это фигура. Фигура имеет размер, а image имеет свой собственный размер. Размеры напрямую не связаны. Например, изображение может быть 1024x786 пикселей, , но фигура, отображающая это изображение, может быть 400x300 точек.

Для отображения изображения в браузере его необходимо масштабировать до размера фигуры. `ScaleImageToShapeSize` Свойство управляет тем, где происходит масштабирование image : в Aspose.Words при экспорте в HTML или в браузере при отображении документа.

Когда`ScaleImageToShapeSize` является`истинный` , изображение масштабируется Aspose.Words с использованием высококачественного масштабирования во время экспорта в HTML. Когда`ScaleImageToShapeSize` это`ЛОЖЬ`, изображение выводится в исходном размере, и браузеру приходится его масштабировать.

В целом браузеры делают быстрое и некачественное масштабирование. В результате вы обычно получите лучшее качество отображения в браузере и меньший размер файла при`ScaleImageToShapeSize` является`истинный` , но лучшее качество печати и более быстрая конвертация при`ScaleImageToShapeSize` является`ЛОЖЬ`.

Помимо фигур, содержащих отдельные растровые изображения, эта опция также влияет на групповые фигуры, состоящие из растровых изображений. Если`ScaleImageToShapeSize` является`ЛОЖЬ` и групповая форма содержит растровые изображения , собственное разрешение которых выше значения, указанного в[`ImageResolution`](../imageresolution/), Aspose.Words will увеличит разрешение рендеринга для этой группы. Это позволяет лучше сохранить качество сгруппированных изображений с высоким разрешением при сохранении в HTML.

## Примеры

Показывает, как отключить масштабирование изображений до размеров их родительской фигуры при сохранении в формате .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте фигуру, содержащую изображение, а затем сделайте эту фигуру значительно меньше изображения.
Shape imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");
imageShape.Width = 50;
imageShape.Height = 50;

// Сохранение документа, содержащего фигуры с изображениями, в HTML приведет к созданию файла изображения в локальной файловой системе.
// для каждой такой фигуры. Выходной HTML-документ будет использовать теги <image> для ссылки на эти изображения и их отображения.
// Когда мы сохраняем документ в HTML, мы можем передать объект SaveOptions, чтобы определить
// следует ли масштабировать все изображения, находящиеся внутри фигур, до размеров их фигур.
// Установка флага "ScaleImageToShapeSize" в значение "true" уменьшит каждое изображение
// к размеру содержащей его фигуры, так что ни одно сохраненное изображение не будет больше, чем того требует документ.
// Установка флага "ScaleImageToShapeSize" в значение "false" сохранит исходные размеры этих изображений,
// что займет больше места в обмен на сохранение качества изображения.
HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);
```

### Смотрите также

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
