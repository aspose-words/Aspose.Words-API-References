---
title: ShapeBase.BehindText
linktitle: BehindText
articleTitle: BehindText
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase BehindText, позволяющее легко управлять наложением фигур в дизайне, улучшая видимость текста и точность макета.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing/shapebase/behindtext/
---
## ShapeBase.BehindText property

Указывает, находится ли фигура под или над текстом.

```csharp
public bool BehindText { get; set; }
```

## Примечания

Действует только для фигур верхнего уровня.

Значение по умолчанию:`ЛОЖЬ`.

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

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
