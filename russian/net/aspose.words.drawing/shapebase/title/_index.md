---
title: ShapeBase.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words для .NET
description: ShapeBase Title свойство. Получает или задает заголовок подпись текущего объекта формы на С#.
type: docs
weight: 530
url: /ru/net/aspose.words.drawing/shapebase/title/
---
## ShapeBase.Title property

Получает или задает заголовок (подпись) текущего объекта формы.

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

// Создайте фигуру, дайте ей название и затем добавьте ее в документ.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.Width = 200;
shape.Height = 200;
shape.Title = "My cube";

builder.InsertNode(shape);

// Когда мы сохраняем документ с фигурой, имеющей заголовок,
// Aspose.Words сохранит этот заголовок в замещающем тексте фигуры.
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
