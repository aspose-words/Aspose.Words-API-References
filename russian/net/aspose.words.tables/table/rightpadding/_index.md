---
title: Table.RightPadding
linktitle: RightPadding
articleTitle: RightPadding
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Table RightPadding для настройки интервала ячеек. Легко настройте правое поле для улучшения макета и читаемости в ваших проектах.
type: docs
weight: 250
url: /ru/net/aspose.words.tables/table/rightpadding/
---
## Table.RightPadding property

Возвращает или задает размер пространства (в пунктах), добавляемого справа от содержимого ячеек.

```csharp
public double RightPadding { get; set; }
```

## Примеры

Показывает, как настроить отступы для содержимого в таблице.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

 // Для каждой ячейки таблицы задайте расстояние между ее содержимым и каждой из ее границ.
// Эта таблица будет поддерживать минимальное расстояние отступа путем переноса текста.
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
