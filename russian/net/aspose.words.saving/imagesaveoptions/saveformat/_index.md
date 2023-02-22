---
title: ImageSaveOptions.SaveFormat
second_title: Справочник по API Aspose.Words для .NET
description: ImageSaveOptions свойство. Указывает формат в котором будут сохранены визуализированные страницы документа или фигуры если используется этот объект параметров сохранения. Может быть растровым Tiff Png Bmp  Jpeg или векторEmf Svg .
type: docs
weight: 130
url: /ru/net/aspose.words.saving/imagesaveoptions/saveformat/
---
## ImageSaveOptions.SaveFormat property

Указывает формат, в котором будут сохранены визуализированные страницы документа или фигуры, если используется этот объект параметров сохранения. Может быть растровым Tiff ,Png ,Bmp , Jpeg или векторEmf ,Svg .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Примечания

На разных платформах поддерживаемые форматы могут отличаться. Количество других опций зависит от выбранного формата.

Также возможно сохранение в SVG как через ImageSaveOptions, так и через[`SvgSaveOptions`](../../svgsaveoptions/).

### Примеры

Показывает, как редактировать изображение, пока Aspose.Words преобразует документ в один.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Когда мы сохраняем документ как изображение, мы можем передать объект SaveOptions в
// редактируем изображение во время его рендеринга операцией сохранения.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Мы можем настроить эти свойства, чтобы изменить яркость и контрастность изображения.
    // Оба имеют шкалу от 0 до 1 и по умолчанию имеют значение 0,5.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // С помощью этих свойств мы можем настроить горизонтальное и вертикальное разрешение.
    // Это повлияет на размеры изображения.
    // Значение по умолчанию для этих свойств — 96,0 для разрешения 96 точек на дюйм.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Мы можем масштабировать изображение, используя это свойство. Значение по умолчанию — 1,0 для масштабирования 100 %.
    // Мы можем использовать это свойство, чтобы отменить любые изменения размеров изображения, которые могут быть вызваны изменением разрешения.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../imagesaveoptions/)
* сборка [Aspose.Words](../../../)


