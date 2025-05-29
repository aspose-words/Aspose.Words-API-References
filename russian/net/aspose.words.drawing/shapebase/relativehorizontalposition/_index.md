---
title: ShapeBase.RelativeHorizontalPosition
linktitle: RelativeHorizontalPosition
articleTitle: RelativeHorizontalPosition
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase RelativeHorizontalPosition, чтобы освоить горизонтальное позиционирование фигур. Оптимизируйте свой дизайн с точностью и контролем!
type: docs
weight: 450
url: /ru/net/aspose.words.drawing/shapebase/relativehorizontalposition/
---
## ShapeBase.RelativeHorizontalPosition property

Указывает, относительно чего фигура расположена горизонтально.

```csharp
public RelativeHorizontalPosition RelativeHorizontalPosition { get; set; }
```

## Примечания

Значение по умолчанию:Column.

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

* enum [RelativeHorizontalPosition](../../relativehorizontalposition/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
