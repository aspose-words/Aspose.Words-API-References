---
title: ShapeBase.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase AllowOverlap, управляйте взаимодействием фигур, включая или отключая перекрытие с другими фигурами для повышения гибкости дизайна.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

Возвращает или задает значение, указывающее, может ли эта фигура перекрывать другие фигуры.

```csharp
public bool AllowOverlap { get; set; }
```

## Примечания

Это свойство влияет на поведение фигуры в Microsoft Word. Aspose.Words игнорирует значение этого свойства.

Это свойство применимо только к фигурам верхнего уровня.

Значение по умолчанию:`истинный`.

## Примеры

Показывает, как работать со свойствами плавающих таблиц.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Для установщика HorizontalAnchor в RelativeHorizontalPosition доступны только Margin, Page, Column.
    // Для любых других значений будет выдано исключение ArgumentException.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Для установщика VerticalAnchor в RelativeVerticalPosition доступны только Margin, Page, Paragraph.
    // Для любых других значений будет выдано исключение ArgumentException.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
