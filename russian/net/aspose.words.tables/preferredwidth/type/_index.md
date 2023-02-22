---
title: PreferredWidth.Type
second_title: Справочник по API Aspose.Words для .NET
description: PreferredWidth свойство. Получает единицу измерения используемую для этого предпочтительного значения ширины.
type: docs
weight: 40
url: /ru/net/aspose.words.tables/preferredwidth/type/
---
## PreferredWidth.Type property

Получает единицу измерения, используемую для этого предпочтительного значения ширины.

```csharp
public PreferredWidthType Type { get; }
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

* enum [PreferredWidthType](../../preferredwidthtype/)
* class [PreferredWidth](../)
* пространство имен [Aspose.Words.Tables](../../preferredwidth/)
* сборка [Aspose.Words](../../../)


