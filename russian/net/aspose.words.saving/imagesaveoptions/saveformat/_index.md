---
title: ImageSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImageSaveOptions SaveFormat, чтобы без труда сохранять документы в таких форматах, как TIFF, PNG, JPEG и др. Улучшите свой рабочий процесс уже сегодня!
type: docs
weight: 140
url: /ru/net/aspose.words.saving/imagesaveoptions/saveformat/
---
## ImageSaveOptions.SaveFormat property

Указывает формат, в котором будут сохранены отрисованные страницы документа или формы, если используется этот объект параметров сохранения. Может быть растровым Tiff ,Png ,Bmp , Jpeg или векторEmf ,Eps , WebP ,Svg .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Примечания

Количество других опций зависит от выбранного формата.

Также, можно сохранить в SVG как через[`ImageSaveOptions`](../) и через[`SvgSaveOptions`](../../svgsaveoptions/).

## Примеры

Показывает, как редактировать изображение, пока Aspose.Words преобразует в него документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Когда мы сохраняем документ как изображение, мы можем передать объект SaveOptions
// редактируем изображение, пока операция сохранения его рендерит.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Мы можем настроить эти свойства, чтобы изменить яркость и контрастность изображения.
    // Оба имеют шкалу от 0 до 1 и по умолчанию равны 0,5.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // С помощью этих свойств мы можем настроить горизонтальное и вертикальное разрешение.
    // Это повлияет на размеры изображения.
    // Значение по умолчанию для этих свойств — 96,0 для разрешения 96 точек на дюйм.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Мы можем масштабировать изображение, используя это свойство. Значение по умолчанию — 1,0, для масштабирования 100%.
    // Мы можем использовать это свойство, чтобы свести на нет любые изменения размеров изображения, которые могут возникнуть при изменении разрешения.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
