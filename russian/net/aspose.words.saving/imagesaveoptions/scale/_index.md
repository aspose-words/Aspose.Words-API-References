---
title: ImageSaveOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImageSaveOptions Scale, позволяющее легко настраивать коэффициент масштабирования изображений, повышая качество и индивидуальность.
type: docs
weight: 150
url: /ru/net/aspose.words.saving/imagesaveoptions/scale/
---
## ImageSaveOptions.Scale property

Получает или задает коэффициент масштабирования для созданных изображений.

```csharp
public float Scale { get; set; }
```

## Примечания

Значение по умолчанию 1.0. Значение должно быть больше 0.

## Примеры

Показывает, как преобразовать объект Office Math в файл изображения в локальной файловой системе.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Создаем объект "ImageSaveOptions" для передачи в метод "Save" рендерера узла для изменения
// как он преобразует узел OfficeMath в изображение.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Установите свойство «Масштаб» на 5, чтобы отрисовать объект в пять раз больше его исходного размера.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

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

* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
