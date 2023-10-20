---
title: ShapeBase.AlternativeText
linktitle: AlternativeText
articleTitle: AlternativeText
second_title: Aspose.Words для .NET
description: ShapeBase AlternativeText свойство. Определяет альтернативный текст который будет отображаться вместо изображения на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

Определяет альтернативный текст, который будет отображаться вместо изображения.

```csharp
public string AlternativeText { get; set; }
```

## Примечания

Значение по умолчанию — пустая строка.

## Примеры

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
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
