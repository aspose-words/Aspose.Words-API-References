---
title: ShapeBase.VerticalAlignment
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase VerticalAlignment, которое оптимизирует вертикальное расположение вашей фигуры для повышения точности дизайна и визуальной привлекательности.
type: docs
weight: 600
url: /ru/net/aspose.words.drawing/shapebase/verticalalignment/
---
## ShapeBase.VerticalAlignment property

Указывает, как фигура располагается по вертикали.

```csharp
public VerticalAlignment VerticalAlignment { get; set; }
```

## Примечания

Значение по умолчанию:None.

Действует только для плавающих фигур верхнего уровня.

## Примеры

Показывает, как вставить плавающее изображение в центр страницы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте плавающее изображение, которое будет отображаться за перекрывающимся текстом, и выровняйте его по центру страницы.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### Смотрите также

* enum [VerticalAlignment](../../verticalalignment/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
