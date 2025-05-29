---
title: ShapeBase.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words для .NET
description: Управляйте свойством заголовка ShapeBase без усилий. Задайте или извлеките заголовок для любого объекта формы, чтобы улучшить ясность и привлекательность вашего дизайна.
type: docs
weight: 570
url: /ru/net/aspose.words.drawing/shapebase/title/
---
## ShapeBase.Title property

Возвращает или задает заголовок (подпись) текущего объекта фигуры.

```csharp
public string Title { get; set; }
```

## Примечания

По умолчанию — пустая строка.

Не может быть`нулевой`, но может быть пустой строкой.

## Примеры

Показывает, как задать заголовок фигуры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте фигуру, дайте ей название, а затем добавьте ее в документ.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.Width = 200;
shape.Height = 200;
shape.Title = "My cube";

builder.InsertNode(shape);

// Когда мы сохраняем документ с формой, имеющей заголовок,
// Aspose.Words сохранит этот заголовок в альтернативном тексте фигуры.
doc.Save(ArtifactsDir + "Shape.Title.docx");

doc = new Document(ArtifactsDir + "Shape.Title.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(string.Empty, shape.Title);
Assert.AreEqual("Title: My cube", shape.AlternativeText);
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
