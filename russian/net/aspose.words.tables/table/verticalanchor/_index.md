---
title: Table.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Table VerticalAnchor для оптимизации позиционирования плавающей таблицы. Узнайте, как улучшить управление макетом с помощью значения Margin по умолчанию.
type: docs
weight: 340
url: /ru/net/aspose.words.tables/table/verticalanchor/
---
## Table.VerticalAnchor property

Получает базовый объект, на основе которого следует рассчитать вертикальное положение плавающей таблицы. Значение по умолчанию:Margin .

```csharp
public RelativeVerticalPosition VerticalAnchor { get; set; }
```

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

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
