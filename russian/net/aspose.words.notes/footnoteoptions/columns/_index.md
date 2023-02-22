---
title: FootnoteOptions.Columns
second_title: Справочник по API Aspose.Words для .NET
description: FootnoteOptions свойство. Указывает количество столбцов в которых форматируется область сносок.
type: docs
weight: 10
url: /ru/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

Указывает количество столбцов, в которых форматируется область сносок.

```csharp
public int Columns { get; set; }
```

### Примечания

Если это свойство имеет значение 0, область сносок форматируется с количеством столбцов на основе количества столбцов на отображаемой странице. Значение по умолчанию: 0. .

### Примеры

Показывает, как разделить раздел сносок на заданное количество столбцов.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### Смотрите также

* class [FootnoteOptions](../)
* пространство имен [Aspose.Words.Notes](../../footnoteoptions/)
* сборка [Aspose.Words](../../../)


