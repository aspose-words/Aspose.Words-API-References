---
title: ImageSaveOptions.PaperColor
second_title: Справочник по API Aspose.Words для .NET
description: ImageSaveOptions свойство. Получает или задает цвет фона бумаги для сгенерированных изображений.
type: docs
weight: 100
url: /ru/net/aspose.words.saving/imagesaveoptions/papercolor/
---
## ImageSaveOptions.PaperColor property

Получает или задает цвет фона (бумаги) для сгенерированных изображений.

Значение по умолчаниюWhite.

```csharp
public Color PaperColor { get; set; }
```

### Примечания

При отображении страниц документа, в котором указан собственный цвет фона, , цвет фона документа переопределит цвет, указанный в этом свойстве.

### Примеры

Преобразует страницу документа Word в изображение с прозрачным или цветным фоном.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Создаем объект "ImageSaveOptions", который мы можем передать в метод "Сохранить" документа
// чтобы изменить способ, которым этот метод преобразует документ в изображение.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// Установите для свойства "PaperColor" прозрачный цвет, чтобы применить прозрачный
// фон для документа при рендеринге его в изображение.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Установите для свойства "PaperColor" непрозрачный цвет, чтобы применить этот цвет
// в качестве фона документа, когда мы визуализируем его в изображение.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### Смотрите также

* class [ImageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../imagesaveoptions/)
* сборка [Aspose.Words](../../../)


