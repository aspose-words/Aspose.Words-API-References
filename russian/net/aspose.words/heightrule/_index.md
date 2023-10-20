---
title: HeightRule Enum
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words для .NET
description: Aspose.Words.HeightRule перечисление. Определяет правило определения высоты объекта на С#.
type: docs
weight: 3130
url: /ru/net/aspose.words/heightrule/
---
## HeightRule enumeration

Определяет правило определения высоты объекта.

```csharp
public enum HeightRule
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| AtLeast | `0` | Высота будет не меньше указанной высоты в пунктах. При необходимости он увеличится до , чтобы вместить весь текст внутри объекта. |
| Exactly | `1` | Высота указывается точно в пунктах. Обратите внимание: если текст не может поместиться внутри объекта этой высоты, он будет обрезан. |
| Auto | `2` | Высота будет увеличиваться автоматически, чтобы разместить весь текст внутри объекта. |

## Примеры

Показывает, как форматировать строки с помощью построителя документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Начинаем вторую строку, а затем настраиваем ее высоту. Разработчик применит эти настройки к
// его текущая строка, а также любые новые строки, которые он создаст впоследствии.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// Первая строка не была затронута реконфигурацией заполнения и по-прежнему содержит значения по умолчанию.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
