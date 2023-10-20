---
title: ShapeBase.BehindText
linktitle: BehindText
articleTitle: BehindText
second_title: Aspose.Words для .NET
description: ShapeBase BehindText свойство. Указывает находится ли фигура ниже или выше текста на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing/shapebase/behindtext/
---
## ShapeBase.BehindText property

Указывает, находится ли фигура ниже или выше текста.

```csharp
public bool BehindText { get; set; }
```

## Примечания

Имеет эффект только для фигур верхнего уровня.

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как вставить плавающее изображение в центр страницы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем плавающее изображение, которое появится за перекрывающимся текстом, и выравниваем его по центру страницы.
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
