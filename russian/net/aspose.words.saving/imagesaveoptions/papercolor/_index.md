---
title: ImageSaveOptions.PaperColor
linktitle: PaperColor
articleTitle: PaperColor
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImageSaveOptions PaperColor, позволяющее легко настраивать цвета фона для созданных изображений, повышая их визуальную привлекательность и уникальность.
type: docs
weight: 110
url: /ru/net/aspose.words.saving/imagesaveoptions/papercolor/
---
## ImageSaveOptions.PaperColor property

Получает или задает цвет фона (бумаги) для созданных изображений.

Значение по умолчанию:White.

```csharp
public Color PaperColor { get; set; }
```

## Примечания

При отображении страниц документа, в котором указан собственный цвет фона, , цвет фона документа переопределит цвет, указанный этим свойством.

## Примеры

Преобразует страницу документа Word в изображение с прозрачным или цветным фоном.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Создаем объект "ImageSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ, которым этот метод преобразует документ в изображение.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);
// Установите свойство "PaperColor" на прозрачный цвет, чтобы применить прозрачный
// фон документа при его рендеринге в изображение.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Установите свойство "PaperColor" на непрозрачный цвет, чтобы применить этот цвет
// в качестве фона документа при его преобразовании в изображение.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### Смотрите также

* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
