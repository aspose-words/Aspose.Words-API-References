---
title: Table.LeftPadding
second_title: Справочник по API Aspose.Words для .NET
description: Table свойство. Получает или задает объем места в пунктах добавляемый слева от содержимого ячеек.
type: docs
weight: 200
url: /ru/net/aspose.words.tables/table/leftpadding/
---
## Table.LeftPadding property

Получает или задает объем места (в пунктах), добавляемый слева от содержимого ячеек.

```csharp
public double LeftPadding { get; set; }
```

### Примеры

Показывает, как настроить заполнение содержимого в таблице.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

 // Для каждой ячейки таблицы задаем расстояние между ее содержимым и каждой из ее границ.
// Эта таблица будет поддерживать минимальное расстояние заполнения путем переноса текста.
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../table/)
* сборка [Aspose.Words](../../../)


