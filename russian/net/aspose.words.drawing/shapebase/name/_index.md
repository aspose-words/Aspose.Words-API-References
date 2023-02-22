---
title: ShapeBase.Name
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Получает или задает необязательное имя формы.
type: docs
weight: 380
url: /ru/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

Получает или задает необязательное имя формы.

```csharp
public string Name { get; set; }
```

### Примечания

По умолчанию пустая строка.

Не может быть нулевым, но может быть пустой строкой.

### Примеры

Показывает, как использовать альтернативный текст фигуры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// Мы можем получить доступ к альтернативному тексту фигуры, щелкнув ее правой кнопкой мыши, а затем через "Форматировать автофигуру" -> > «Альтернативный текст».
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Сохраняем документ в HTML, а затем удаляем связанное изображение, принадлежащее нашей фигуре.
// Браузер, читающий наш HTML, отобразит замещающий текст вместо отсутствующего изображения.
doc.Save(ArtifactsDir + "Shape.AltText.html");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


