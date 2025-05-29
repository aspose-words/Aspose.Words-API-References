---
title: Table.TextWrapping
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Table TextWrapping, чтобы легко управлять потоком текста в таблицах. Улучшите читаемость и дизайн с помощью гибких текстовых опций!
type: docs
weight: 310
url: /ru/net/aspose.words.tables/table/textwrapping/
---
## Table.TextWrapping property

Получает или устанавливает`TextWrapping` для таблицы.

```csharp
public TextWrapping TextWrapping { get; set; }
```

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

* enum [TextWrapping](../../textwrapping/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
