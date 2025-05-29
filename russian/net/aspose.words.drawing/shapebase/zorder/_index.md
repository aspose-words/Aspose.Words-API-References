---
title: ShapeBase.ZOrder
linktitle: ZOrder
articleTitle: ZOrder
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ShapeBase ZOrder улучшает ваш дизайн, управляя порядком отображения перекрывающихся фигур для более четкого и организованного макета.
type: docs
weight: 650
url: /ru/net/aspose.words.drawing/shapebase/zorder/
---
## ShapeBase.ZOrder property

Определяет порядок отображения перекрывающихся фигур.

```csharp
public int ZOrder { get; set; }
```

## Примечания

Действует только для фигур верхнего уровня.

Значение по умолчанию — 0.

Число представляет собой приоритет стекирования. Фигура с большим числом будет отображаться как , как если бы она перекрывала («перед») фигуру с меньшим числом.

Порядок перекрывающихся фигур независим для фигур в заголовке и в тексте main документа.

Порядок отображения дочерних фигур в групповой фигуре определяется их order внутри групповой фигуры.

## Примеры

Показывает, как управлять порядком фигур.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте три прямоугольника разного цвета, которые частично перекрывают друг друга.
// Когда мы вставляем фигуру, которая перекрывает другую фигуру, Aspose.Words помещает новую фигуру поверх старой.
// Светло-зеленый прямоугольник перекроет светло-голубой прямоугольник и частично закроет его,
// и светло-голубой прямоугольник закроет оранжевый прямоугольник.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);
shape.FillColor = Color.Orange;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 150,
    RelativeVerticalPosition.TopMargin, 150, 200, 200, WrapType.None);
shape.FillColor = Color.LightBlue;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 200, 200, WrapType.None);
shape.FillColor = Color.LightGreen;

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

// Свойство «ZOrder» фигуры определяет ее приоритет размещения среди других перекрывающихся фигур.
// Если две перекрывающиеся фигуры имеют разные значения "ZOrder",
 // Microsoft Word поместит фигуру с большим значением над фигурой с меньшим значением.
// Задайте значения "ZOrder" наших фигур, чтобы поместить первый оранжевый прямоугольник над вторым светло-голубым
// и второй светло-голубой прямоугольник над третьим светло-зеленым прямоугольником.
// Это изменит их первоначальный порядок размещения.
shapes[0].ZOrder = 3;
shapes[1].ZOrder = 2;
shapes[2].ZOrder = 1;

doc.Save(ArtifactsDir + "Shape.ZOrder.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
