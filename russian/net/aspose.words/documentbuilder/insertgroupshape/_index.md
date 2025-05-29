---
title: DocumentBuilder.InsertGroupShape
linktitle: InsertGroupShape
articleTitle: InsertGroupShape
second_title: Aspose.Words для .NET
description: Группируйте фигуры без усилий с помощью метода InsertGroupShape в DocumentBuilder. Создавайте организованные проекты, вставляя новые узлы GroupShape без проблем.
type: docs
weight: 360
url: /ru/net/aspose.words/documentbuilder/insertgroupshape/
---
## InsertGroupShape(*params ShapeBase[]*) {#insertgroupshape}

Группирует фигуры, переданные в качестве параметра, в новый узел GroupShape, который вставляется в текущую позицию.

```csharp
public GroupShape InsertGroupShape(params ShapeBase[] shapes)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| shapes | ShapeBase[] | Список фигур для группировки. |

## Примечания

Положение и размеры новой GroupShape будут рассчитаны автоматически.

Формы VML и DML нельзя группировать вместе.

## Примеры

Показывает, как сочетать форму группы с формой.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Объединяем фигуры в узел GroupShape, который вставляется в указанную позицию.
GroupShape groupShape1 = builder.InsertGroupShape(shape1, shape2);

// Объединяем узлы Shape и GroupShape.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(groupShape1, shape3);

doc.Save(ArtifactsDir + "Shape.CombineGroupShape.docx");
```

Показывает, как вставить групповую фигуру DML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Размеры нового узла GroupShape.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Вставляем узел GroupShape указанного размера, который вставляется в указанную позицию.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// Вставьте узел GroupShape, положение и размер которого будут рассчитаны автоматически.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### Смотрите также

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertGroupShape(*double, double, double, double, params ShapeBase[]*) {#insertgroupshape_1}

Группирует фигуры, переданные в качестве параметра, в новый узел GroupShape указанного размера, который вставляется в указанную позицию.

```csharp
public GroupShape InsertGroupShape(double left, double top, double width, double height, 
    params ShapeBase[] shapes)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| left | Double | Расстояние в точках от начала координат до левой стороны групповой фигуры. |
| top | Double | Расстояние в точках от начала координат до верхней стороны групповой фигуры. |
| width | Double | Ширина групповой фигуры в точках. Отрицательное значение не допускается. |
| height | Double | Высота групповой фигуры в пунктах. Отрицательное значение не допускается. |
| shapes | ShapeBase[] | Список фигур для группировки. |

## Примечания

Формы VML и DML не могут быть сгруппированы вместе.

## Примеры

Показывает, как вставить групповую фигуру DML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Размеры нового узла GroupShape.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Вставляем узел GroupShape указанного размера, который вставляется в указанную позицию.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// Вставьте узел GroupShape, положение и размер которого будут рассчитаны автоматически.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### Смотрите также

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
