---
title: ShapeBase.AlternativeText
linktitle: AlternativeText
articleTitle: AlternativeText
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase AlternativeText, которое повышает доступность, предоставляя описательный текст для графики, улучшая пользовательский опыт и SEO.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

Определяет альтернативный текст, отображаемый вместо графики.

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

// Мы можем получить доступ к альтернативному тексту фигуры, щелкнув ее правой кнопкой мыши, а затем через «Формат автофигуры» -> «Альтернативный текст».
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Сохраните документ в формате HTML, а затем удалите связанное изображение, принадлежащее нашей фигуре.
// Браузер, считывающий наш HTML, отобразит альтернативный текст вместо отсутствующего изображения.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
