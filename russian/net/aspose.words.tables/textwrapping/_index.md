---
title: TextWrapping Enum
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Tables.TextWrapping для эффективного обтекания таблиц текстом. Улучшите форматирование документа с легкостью!
type: docs
weight: 7230
url: /ru/net/aspose.words.tables/textwrapping/
---
## TextWrapping enumeration

Указывает, как текст обтекает таблицу.

```csharp
public enum TextWrapping
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Текст и таблица отображаются в порядке их появления в документе. |
| Around | `1` | Текст обтекает таблицу, занимая доступное боковое пространство. |
| Default | `0` | Значение по умолчанию. |

## Примеры

Показывает, как работать с переносом текста в таблице.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

builder.Font.Size = 16;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Установите свойство "TextWrapping" на "TextWrapping.Around", чтобы таблица оборачивала текст вокруг себя,
// и переместите его в абзац ниже, установив позицию.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Tables](../../aspose.words.tables/)
* сборка [Aspose.Words](../../)
