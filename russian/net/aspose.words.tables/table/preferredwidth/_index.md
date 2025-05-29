---
title: Table.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words для .NET
description: Узнайте, как использовать свойство Table PreferredWidth, чтобы легко настроить и оптимизировать макет таблицы для улучшения дизайна и удобства пользователя.
type: docs
weight: 220
url: /ru/net/aspose.words.tables/table/preferredwidth/
---
## Table.PreferredWidth property

Получает или задает предпочтительную ширину таблицы.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## Примечания

Значение по умолчанию:[`Auto`](../../preferredwidth/auto/).

## Примеры

Показывает, как настроить автоматическое подгонку таблицы под ширину страницы (50%).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

### Смотрите также

* class [PreferredWidth](../../preferredwidth/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
