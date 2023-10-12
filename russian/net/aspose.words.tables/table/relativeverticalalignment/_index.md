---
title: Table.RelativeVerticalAlignment
second_title: Справочник по API Aspose.Words для .NET
description: Table свойство. Получает или задает относительное вертикальное выравнивание плавающей таблицы.
type: docs
weight: 240
url: /ru/net/aspose.words.tables/table/relativeverticalalignment/
---
## Table.RelativeVerticalAlignment property

Получает или задает относительное вертикальное выравнивание плавающей таблицы.

```csharp
public VerticalAlignment RelativeVerticalAlignment { get; set; }
```

### Примеры

Показывает, как задать расположение плавающих таблиц.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 1, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// Установите местоположение таблицы в нужном месте на странице, например, в данном случае в правом нижнем углу.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

 // Мы также можем установить горизонтальное и вертикальное смещение в пунктах от места абзаца, куда мы вставили таблицу.
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### Смотрите также

* enum [VerticalAlignment](../../../aspose.words.drawing/verticalalignment/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../table/)
* сборка [Aspose.Words](../../../)


