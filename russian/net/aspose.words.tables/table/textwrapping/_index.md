---
title: Table.TextWrapping
second_title: Справочник по API Aspose.Words для .NET
description: Table свойство. Получает или устанавливаетTextWrapping для таблицы.
type: docs
weight: 310
url: /ru/net/aspose.words.tables/table/textwrapping/
---
## Table.TextWrapping property

Получает или устанавливает`TextWrapping` для таблицы.

```csharp
public TextWrapping TextWrapping { get; set; }
```

### Примеры

Показывает, как работать с переносом текста таблицы.

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

// Установите для свойства "TextWrapping" значение "TextWrapping.Around", чтобы таблица оборачивала текст вокруг себя,
// и вставьте его в абзац ниже, установив позицию.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### Смотрите также

* enum [TextWrapping](../../textwrapping/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../table/)
* сборка [Aspose.Words](../../../)


