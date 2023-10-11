---
title: PreferredWidth.Value
second_title: Справочник по API Aspose.Words для .NET
description: PreferredWidth свойство. Получает предпочтительное значение ширины. Единица измерения указана в п.Type свойство.
type: docs
weight: 50
url: /ru/net/aspose.words.tables/preferredwidth/value/
---
## PreferredWidth.Value property

Получает предпочтительное значение ширины. Единица измерения указана в п.[`Type`](../type/) свойство.

```csharp
public double Value { get; }
```

### Примеры

Показывает, как проверить предпочтительный тип ширины и значение ячейки таблицы.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### Смотрите также

* class [PreferredWidth](../)
* пространство имен [Aspose.Words.Tables](../../preferredwidth/)
* сборка [Aspose.Words](../../../)


