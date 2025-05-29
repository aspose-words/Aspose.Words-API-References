---
title: ShapeBase.LocalToParent
linktitle: LocalToParent
articleTitle: LocalToParent
second_title: Aspose.Words для .NET
description: Преобразуйте локальные координаты в родительское пространство форм с помощью метода ShapeBase LocalToParent. Повысьте точность в своих проектах 3D-моделирования уже сегодня!
type: docs
weight: 680
url: /ru/net/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase.LocalToParent method

Преобразует значение из локального координатного пространства в координатное пространство родительской фигуры.

```csharp
public PointF LocalToParent(PointF value)
```

## Примеры

Показывает, как перевести координаты x и y на координатной плоскости фигуры в координатную плоскость родительской фигуры.

```csharp
Document doc = new Document();

// Вставьте групповую фигуру и разместите ее на 100 пунктов ниже и правее
// исходная точка координат x и Y документа.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Используйте метод "LocalToParent", чтобы определить (0, 0) во внутренних координатах x и y группы
// лежит на (100, 100) системы координат родительской фигуры. Родителем групповой фигуры является сам документ.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// По умолчанию внутренняя координатная плоскость фигуры имеет верхний левый угол в точке (0, 0),
// и нижний правый угол в (1000, 1000). Из-за своего размера наша групповая фигура занимает область 500pt x 500pt
// в плоскости документа. Это означает, что перемещение на 1pt в координатной плоскости документа переместит
// к перемещению на 2 точки на координатной плоскости групповой фигуры.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Перемещаем начало осей x и y групповой фигуры из верхнего левого угла в центр.
// Это еще больше сместит внутренние координаты группы относительно координат документа.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// Изменение масштаба координатной плоскости также повлияет на относительное местоположение.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Если мы хотим добавить фигуру в эту группу, определив ее местоположение на основе местоположения в документе,
// нам сначала нужно будет подтвердить местоположение в форме группы, которое будет соответствовать местоположению документа.
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
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
