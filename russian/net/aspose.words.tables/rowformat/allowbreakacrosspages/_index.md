---
title: RowFormat.AllowBreakAcrossPages
second_title: Справочник по API Aspose.Words для .NET
description: RowFormat свойство. Истинно если тексту в строке таблицы разрешено разделение по разрыву страницы.
type: docs
weight: 10
url: /ru/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

Истинно, если тексту в строке таблицы разрешено разделение по разрыву страницы.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

### Примеры

Показывает, как отключить разбивку строк по страницам для каждой строки таблицы.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Установите для свойства «AllowBreakAcrossPages» значение «false», чтобы сохранить строку
// целиком, если таблица занимает две страницы, которые разбиваются по этой строке.
// Если строка слишком велика и не помещается на одной странице, Microsoft Word переместит ее на следующую страницу.
// Установите для свойства «AllowBreakAcrossPages» значение «true», чтобы разрешить разбивку строки на две страницы.
foreach (Row row in table.OfType<Row>())
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Смотрите также

* class [RowFormat](../)
* пространство имен [Aspose.Words.Tables](../../rowformat/)
* сборка [Aspose.Words](../../../)


