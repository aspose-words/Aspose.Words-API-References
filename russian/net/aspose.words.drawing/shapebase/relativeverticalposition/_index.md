---
title: ShapeBase.RelativeVerticalPosition
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Указывает относительно того как фигура расположена по вертикали.
type: docs
weight: 440
url: /ru/net/aspose.words.drawing/shapebase/relativeverticalposition/
---
## ShapeBase.RelativeVerticalPosition property

Указывает относительно того, как фигура расположена по вертикали.

```csharp
public RelativeVerticalPosition RelativeVerticalPosition { get; set; }
```

### Примечания

Значение по умолчанию:Paragraph.

Имеет эффект только для плавающих фигур верхнего уровня.

### Примеры

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

* enum [RelativeVerticalPosition](../../relativeverticalposition/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


