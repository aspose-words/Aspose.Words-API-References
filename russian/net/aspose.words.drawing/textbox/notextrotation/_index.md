---
title: TextBox.NoTextRotation
second_title: Справочник по API Aspose.Words для .NET
description: TextBox свойство. Получает или задает логическое значение указывающее что текст TextBox не должен вращаться при повороте фигуры.
type: docs
weight: 80
url: /ru/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

Получает или задает логическое значение, указывающее, что текст TextBox не должен вращаться при повороте фигуры.

```csharp
public bool NoTextRotation { get; set; }
```

### Примечания

Значение по умолчанию:`ЛОЖЬ`

### Примеры

Показывает, как отключить поворот текста при повороте фигуры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Ellipse, 20, 20);
shape.TextBox.NoTextRotation = true;

doc.Save(ArtifactsDir + "Shape.NoTextRotation.docx");
```

### Смотрите также

* class [TextBox](../)
* пространство имен [Aspose.Words.Drawing](../../textbox/)
* сборка [Aspose.Words](../../../)


