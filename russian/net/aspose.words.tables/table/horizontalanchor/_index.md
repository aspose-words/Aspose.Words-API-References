---
title: Table.HorizontalAnchor
linktitle: HorizontalAnchor
articleTitle: HorizontalAnchor
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Table HorizontalAnchor для оптимизации позиционирования плавающей таблицы. Легко настраивайте горизонтальное выравнивание для улучшенного управления макетом.
type: docs
weight: 170
url: /ru/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

Получает базовый объект, на основе которого следует рассчитать горизонтальное положение плавающей таблицы. Значение по умолчанию:Column .

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
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

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
