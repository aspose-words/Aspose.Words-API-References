---
title: ShapeBase.AllowOverlap
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Получает или задает значение указывающее может ли эта фигура перекрывать другие фигуры.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

Получает или задает значение, указывающее, может ли эта фигура перекрывать другие фигуры.

```csharp
public bool AllowOverlap { get; set; }
```

### Примечания

Это свойство влияет на поведение фигуры в Microsoft Word. Aspose.Words игнорирует значение этого свойства.

Это свойство применимо только к фигурам верхнего уровня.

Значение по умолчанию:`истинный`.

### Примеры

Показывает, как работать со свойствами плавающих таблиц.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // В RelativeHorizontalPosition для установки HorizontalAnchor доступны только поля, страницы и столбцы.
    // Для любых других значений будет выброшено исключение ArgumentException.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Только поле, страница и абзац доступны в RelativeVerticalPosition для средства установки вертикальной привязки.
    // Для любых других значений будет выброшено исключение ArgumentException.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


