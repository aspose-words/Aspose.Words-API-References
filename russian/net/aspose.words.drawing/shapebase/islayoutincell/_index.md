---
title: ShapeBase.IsLayoutInCell
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Получает или задает флаг указывающий отображается ли фигура внутри таблицы или за ее пределами.
type: docs
weight: 310
url: /ru/net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

Получает или задает флаг, указывающий, отображается ли фигура внутри таблицы или за ее пределами.

```csharp
public bool IsLayoutInCell { get; set; }
```

### Примечания

Значение по умолчанию:`истинный`.

Имеет эффект только для фигур верхнего уровня, свойство[`WrapType`](../wraptype/) из которых установлено значение value , отличное от[`Inline`](../../../aspose.words/inline/).

### Примеры

Показывает, как определить способ отображения фигуры в ячейке таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 10;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Single;

table.Style = tableStyle;

builder.MoveTo(table.FirstRow.FirstCell.FirstParagraph);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);

// Установите для свойства IsLayoutInCell значение «true», чтобы отобразить фигуру как встроенный элемент внутри абзаца ячейки.
// Началом координат, которое будет определять местоположение фигуры, будет левый верхний угол ячейки фигуры.
// Если мы изменим размер ячейки, фигура переместится, сохраняя ту же позицию, начиная с верхнего левого угла ячейки.
// Установите для свойства IsLayoutInCell значение «false», чтобы отобразить фигуру как независимую плавающую фигуру.
// Начало координат, которое будет определять местоположение фигуры, будет верхний левый угол страницы,
// и фигура не будет реагировать на изменение размера ячейки.
shape.IsLayoutInCell = isLayoutInCell;

// Мы можем применить свойство IsLayoutInCell только к плавающим фигурам.
shape.WrapType = WrapType.None;

doc.Save(ArtifactsDir + "Shape.LayoutInTableCell.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


