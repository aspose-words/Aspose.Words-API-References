---
title: ShapeBase.IsLayoutInCell
linktitle: IsLayoutInCell
articleTitle: IsLayoutInCell
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase IsLayoutInCell, управляйте размещением фигур в таблицах для повышения гибкости дизайна и улучшения управления макетом.
type: docs
weight: 330
url: /ru/net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

Возвращает или задает флаг, указывающий, отображается ли фигура внутри таблицы или вне ее.

```csharp
public bool IsLayoutInCell { get; set; }
```

## Примечания

Значение по умолчанию:`истинный`.

Действует только для фигур верхнего уровня, свойство[`WrapType`](../wraptype/) из которых установлено значение value , отличное от[`Inline`](../../../aspose.words/inline/).

## Примеры

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

// Установите свойство "IsLayoutInCell" в значение "true", чтобы отобразить фигуру как встроенный элемент внутри абзаца ячейки.
// Начало координат, определяющее местоположение фигуры, будет находиться в верхнем левом углу ячейки фигуры.
// Если изменить размер ячейки, фигура переместится, сохраняя то же положение, начиная с верхнего левого угла ячейки.
// Установите свойство "IsLayoutInCell" в значение "false", чтобы отобразить фигуру как независимую плавающую фигуру.
// Начало координат, которое определит местоположение фигуры, будет находиться в верхнем левом углу страницы,
// и фигура не будет реагировать на изменение размера ее ячейки.
shape.IsLayoutInCell = isLayoutInCell;

// Свойство «IsLayoutInCell» можно применять только к плавающим фигурам.
shape.WrapType = WrapType.None;

doc.Save(ArtifactsDir + "Shape.LayoutInTableCell.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
