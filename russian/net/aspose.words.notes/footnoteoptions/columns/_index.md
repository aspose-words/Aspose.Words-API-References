---
title: FootnoteOptions.Columns
linktitle: Columns
articleTitle: Columns
second_title: Aspose.Words для .NET
description: FootnoteOptions Columns свойство. Указывает количество столбцов с помощью которых форматируется область сносок на С#.
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

Если это свойство имеет значение 0, область сносок форматируется с использованием количества столбцов, основанного на количестве столбцов на отображаемой странице. Значение по умолчанию — 0. .

## Примеры

Показывает, как разделить раздел сносок на заданное количество столбцов.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### Смотрите также

* class [FootnoteOptions](../)
* пространство имен [Aspose.Words.Notes](../../../aspose.words.notes/)
* сборка [Aspose.Words](../../../)
