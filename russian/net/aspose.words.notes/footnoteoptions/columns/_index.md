---
title: FootnoteOptions.Columns
linktitle: Columns
articleTitle: Columns
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FootnoteOptions Columns, чтобы легко форматировать сноски с помощью настраиваемых макетов столбцов для улучшения читабельности и наглядности.
type: docs
weight: 10
url: /ru/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

Указывает количество столбцов, с помощью которых форматируется область сносок.

```csharp
public int Columns { get; set; }
```

## Примечания

Если это свойство имеет значение 0, область сносок форматируется с числом столбцов на основе числа столбцов на отображаемой странице. Значение по умолчанию — 0.

## Примеры

Показывает, как разбить раздел сносок на заданное количество столбцов.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### Смотрите также

* class [FootnoteOptions](../)
* пространство имен [Aspose.Words.Notes](../../../aspose.words.notes/)
* сборка [Aspose.Words](../../../)
