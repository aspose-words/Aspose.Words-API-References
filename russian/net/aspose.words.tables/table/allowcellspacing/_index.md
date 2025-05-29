---
title: Table.AllowCellSpacing
linktitle: AllowCellSpacing
articleTitle: AllowCellSpacing
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Table AllowCellSpacing, чтобы легко управлять интервалом ячеек в макетах. Улучшите свой дизайн с помощью настраиваемых параметров!
type: docs
weight: 60
url: /ru/net/aspose.words.tables/table/allowcellspacing/
---
## Table.AllowCellSpacing property

Возвращает или задает параметр «Разрешить интервал между ячейками».

```csharp
public bool AllowCellSpacing { get; set; }
```

## Примеры

Показывает, как включить интервал между отдельными ячейками в таблице.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Animal");
builder.InsertCell();
builder.Write("Class");
builder.EndRow();
builder.InsertCell();
builder.Write("Dog");
builder.InsertCell();
builder.Write("Mammal");
builder.EndTable();

table.CellSpacing = 3;

// Установите свойство «AllowCellSpacing» в значение «true», чтобы включить интервал между ячейками
// с величиной, равной значению свойства "CellSpacing" в пунктах.
// Установите свойство «AllowCellSpacing» на «false», чтобы отключить интервал между ячейками
// и игнорировать значение свойства "CellSpacing".
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// Настройка свойства «CellSpacing» автоматически включит интервал между ячейками.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
