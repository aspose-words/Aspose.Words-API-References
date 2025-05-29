---
title: RowFormat.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: Aspose.Words для .NET
description: Откройте для себя свойство RowFormat AllowBreakAcrossPages, обеспечивающее плавное перемещение текста в строках таблицы через разрывы страниц для улучшения читаемости и наглядности.
type: docs
weight: 10
url: /ru/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

Истинно, если текст в строке таблицы может быть разделен на разрыв страницы.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

## Примеры

Показывает, как отключить разбиение строк по страницам для каждой строки в таблице.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Установите свойство «AllowBreakAcrossPages» в значение «false», чтобы сохранить строку
// как единое целое, если таблица занимает две страницы, которые разбиваются по этой строке.
// Если строка слишком велика для размещения на одной странице, Microsoft Word перенесет ее на следующую страницу.
// Установите свойство «AllowBreakAcrossPages» в значение «true», чтобы разрешить разбиение строки на две страницы.
foreach (Row row in table)
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Смотрите также

* class [RowFormat](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
