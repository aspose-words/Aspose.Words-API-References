---
title: ShapeBase.LocalToParent
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase метод. Преобразует значение из локального координатного пространства в координатное пространство родительской фигуры.
type: docs
weight: 670
url: /ru/net/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase.LocalToParent method

Преобразует значение из локального координатного пространства в координатное пространство родительской фигуры.

```csharp
public PointF LocalToParent(PointF value)
```

### Примеры

Показывает, как преобразовать местоположение координат X и Y на координатной плоскости фигуры в местоположение на координатной плоскости родительской фигуры.

```csharp
Document doc = new Document();

// Вставляем фигуру группы и размещаем ее на 100 пунктов ниже и правее
// исходная точка координат x и Y документа.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Используйте метод «LocalToParent», чтобы определить, что (0, 0) во внутренних координатах x и y группы
// лежит в (100, 100) системы координат родительской фигуры. Родителем формы группы является сам документ.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// По умолчанию внутренняя координатная плоскость фигуры имеет верхний левый угол (0, 0),
// и нижний правый угол (1000, 1000). Из-за своего размера наша групповая фигура занимает площадь 500 x 500 пикселей.
// в плоскости документа. Это означает, что перемещение на 1 пт в координатной плоскости документа будет смещаться.
// к перемещению на 2 пункта по координатной плоскости группы.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Перемещаем начало осей x и y фигуры группы из верхнего левого угла в центр.
// Это еще больше сместит внутренние координаты группы относительно координат документа.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// Изменение масштаба координатной плоскости также повлияет на относительные местоположения.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Если мы хотим добавить фигуру в эту группу, определяя ее местоположение на основе местоположения в документе,
// нам нужно сначала подтвердить местоположение в форме группы, которое будет соответствовать местоположению документа.
Assert.AreEqual(new PointF(700, 700), group.LocalToParent(new PointF(350, 350)));

Shape shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

group.AppendChild(shape);
doc.FirstSection.Body.FirstParagraph.AppendChild(group);

doc.Save(ArtifactsDir + "Shape.LocalToParent.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


