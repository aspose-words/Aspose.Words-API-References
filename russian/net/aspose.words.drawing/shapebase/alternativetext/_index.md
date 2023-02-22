---
title: ShapeBase.AlternativeText
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Определяет альтернативный текст который будет отображаться вместо графики.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

Определяет альтернативный текст, который будет отображаться вместо графики.

```csharp
public string AlternativeText { get; set; }
```

### Примечания

Значение по умолчанию — пустая строка.

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


