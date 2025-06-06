---
title: ShapeBase.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase Name, которое позволяет легко управлять дополнительными именами фигур, повышая гибкость проектирования и организацию проекта.
type: docs
weight: 420
url: /ru/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

Получает или задает необязательное имя фигуры.

```csharp
public string Name { get; set; }
```

## Примечания

По умолчанию — пустая строка.

Не может быть`нулевой`, но может быть пустой строкой.

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
