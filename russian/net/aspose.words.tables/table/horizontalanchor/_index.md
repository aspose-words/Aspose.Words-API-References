---
title: Table.HorizontalAnchor
second_title: Справочник по API Aspose.Words для .NET
description: Table свойство. Получает базовый объект на основе которого должно рассчитываться горизонтальное положение плавающей таблицы. Значение по умолчаниюColumn .
type: docs
weight: 170
url: /ru/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

Получает базовый объект, на основе которого должно рассчитываться горизонтальное положение плавающей таблицы. Значение по умолчанию:Column .

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
```

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

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../table/)
* сборка [Aspose.Words](../../../)


