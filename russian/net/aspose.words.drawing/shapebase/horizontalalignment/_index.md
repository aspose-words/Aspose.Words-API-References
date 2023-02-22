---
title: ShapeBase.HorizontalAlignment
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Определяет горизонтальное расположение фигуры.
type: docs
weight: 210
url: /ru/net/aspose.words.drawing/shapebase/horizontalalignment/
---
## ShapeBase.HorizontalAlignment property

Определяет горизонтальное расположение фигуры.

```csharp
public HorizontalAlignment HorizontalAlignment { get; set; }
```

### Примечания

Значение по умолчаниюNone.

Имеет эффект только для плавающих фигур верхнего уровня.

### Примеры

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

* enum [HorizontalAlignment](../../horizontalalignment/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


