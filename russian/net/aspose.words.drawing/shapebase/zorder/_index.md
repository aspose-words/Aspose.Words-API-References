---
title: ShapeBase.ZOrder
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Определяет порядок отображения перекрывающихся фигур.
type: docs
weight: 550
url: /ru/net/aspose.words.drawing/shapebase/zorder/
---
## ShapeBase.ZOrder property

Определяет порядок отображения перекрывающихся фигур.

```csharp
public int ZOrder { get; set; }
```

### Примечания

Имеет эффект только для фигур верхнего уровня.

Значение по умолчанию — 0.

Число представляет приоритет стека. Фигура с более высоким номером будет отображаться так, как если бы она перекрывала (перед) фигуру с меньшим номером.

Порядок перекрывающихся фигур независим для фигур в заголовке и в тексте main документа.

Порядок отображения дочерних фигур в фигуре группы определяется их order внутри фигуры группы.

### Примеры

Показывает, как управлять порядком фигур.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем три прямоугольника разного цвета, которые частично перекрывают друг друга.
// Когда мы вставляем фигуру, которая перекрывает другую фигуру, Aspose.Words помещает новую фигуру поверх старой.
// Светло-зеленый прямоугольник наложится на светло-синий прямоугольник и частично закроет его,
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

// Свойство "ZOrder" фигуры определяет ее приоритет в стеке среди других перекрывающихся фигур.
// Если две перекрывающиеся фигуры имеют разные значения "ZOrder",
 // Microsoft Word поместит фигуру с более высоким значением над фигурой с более низким значением.
// Установите значения "ZOrder" наших фигур, чтобы разместить первый оранжевый прямоугольник над вторым голубым.
// и второй голубой прямоугольник над третьим светло-зеленым прямоугольником.
// Это изменит их первоначальный порядок наложения.
shapes[0].ZOrder = 3;
shapes[1].ZOrder = 2;
shapes[2].ZOrder = 1;

doc.Save(ArtifactsDir + "Shape.ZOrder.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


