---
title: ShapeBase.Name
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Получает или задает необязательное имя фигуры.
type: docs
weight: 400
url: /ru/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

Получает или задает необязательное имя фигуры.

```csharp
public string Name { get; set; }
```

### Примечания

По умолчанию — пустая строка.

Не может быть`нулевой`, но может быть пустой строкой.

### Примеры

Показывает, как использовать альтернативный текст фигуры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// Мы можем получить доступ к альтернативному тексту фигуры, щелкнув его правой кнопкой мыши, а затем выбрав «Формат автофигуры» -> gt; «Альтернативный текст».
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Сохраняем документ в HTML, а затем удаляем связанное изображение, принадлежащее нашей фигуре.
// Браузер, читающий наш HTML, отобразит замещающий текст вместо отсутствующего изображения.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


