---
title: Enum PreferredWidthType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Tables.PreferredWidthType перечисление. Указывает единицу измерения предпочтительной ширины таблицы или ячейки.
type: docs
weight: 6000
url: /ru/net/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enumeration

Указывает единицу измерения предпочтительной ширины таблицы или ячейки.

```csharp
public enum PreferredWidthType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Auto | `1` | Предпочтительная ширина не указана. Фактическая ширина таблицы или ячейки либо указывается явной шириной, либо будет определяться автоматически алгоритмом компоновки таблицы при отображении таблицы, в зависимости от настройки автоподбора таблицы. |
| Percent | `2` | Измерить ширину текущего элемента, используя указанный процент. |
| Points | `3` | Измерить ширину текущего элемента, используя указанное количество точек (1/72 дюйма). |

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

* class [PreferredWidth](../preferredwidth/)
* пространство имен [Aspose.Words.Tables](../../aspose.words.tables/)
* сборка [Aspose.Words](../../)


