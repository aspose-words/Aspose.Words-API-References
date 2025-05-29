---
title: SoftEdgeFormat Class
linktitle: SoftEdgeFormat
articleTitle: SoftEdgeFormat
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.SoftEdgeFormat, чтобы улучшить ваши документы с помощью потрясающих эффектов смягчения краев, придавая им профессиональный вид.
type: docs
weight: 1710
url: /ru/net/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class

Представляет форматирование мягких краев для объекта.

```csharp
public class SoftEdgeFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Radius](../../aspose.words.drawing/softedgeformat/radius/) { get; set; } | Возвращает или задает двойное значение, представляющее длину радиуса для эффекта мягкого края в пунктах (pt). Значение по умолчанию — 0.0. |

## Методы

| Имя | Описание |
| --- | --- |
| [Remove](../../aspose.words.drawing/softedgeformat/remove/)() | Удаляет`SoftEdgeFormat` из родительского объекта. |

## Примечания

Используйте[`SoftEdge`](../shapebase/softedge/) свойство для доступа к свойствам мягкого края объекта. Вы не создаете экземпляры`SoftEdgeFormat` класс напрямую.

## Примеры

Показывает, как работать с форматированием с мягкими краями.

```csharp
DocumentBuilder builder = new DocumentBuilder();
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 200);

// Применить мягкие края к фигуре.
shape.SoftEdge.Radius = 30;

builder.Document.Save(ArtifactsDir + "Shape.SoftEdge.docx");

// Загрузить документ с прямоугольной формой и мягкими краями.
Document doc = new Document(ArtifactsDir + "Shape.SoftEdge.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
SoftEdgeFormat softEdgeFormat = shape.SoftEdge;

// Проверьте радиус скругления кромок.
Assert.AreEqual(30, softEdgeFormat.Radius);

// Удалить мягкие края из фигуры.
softEdgeFormat.Remove();

// Проверьте радиус удаленного мягкого края.
Assert.AreEqual(0, softEdgeFormat.Radius);
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
