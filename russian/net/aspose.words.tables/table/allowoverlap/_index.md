---
title: Table.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words для .NET
description: Table AllowOverlap свойство. Определяет должна ли плавающая таблица позволять другим плавающим объектам в документе перекрывать ее экстенты при отображении. Значение по умолчаниюистинный  на С#.
type: docs
weight: 70
url: /ru/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

Определяет, должна ли плавающая таблица позволять другим плавающим объектам в документе перекрывать ее экстенты при отображении. Значение по умолчанию:`истинный` .

```csharp
public bool AllowOverlap { get; }
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

    // В RelativeHorizontalPosition для установки HorizontalAnchor доступны только поля, страницы и столбцы.
    // Для любых других значений будет выброшено исключение ArgumentException.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Только поле, страница и абзац доступны в RelativeVerticalPosition для средства установки вертикальной привязки.
    // Для любых других значений будет выброшено исключение ArgumentException.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
