---
title: Cell.ParentRow
second_title: Справочник по API Aspose.Words для .NET
description: Cell свойство. Возвращает родительскую строку ячейки.
type: docs
weight: 90
url: /ru/net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

Возвращает родительскую строку ячейки.

```csharp
public Row ParentRow { get; }
```

### Примечания

Эквивалентно`(Строка)FirstNonMarkupParentNode`.

### Примеры

Показывает, как накрыть стол, чтобы оставаться вместе на одной странице.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Включение KeepWithNext для каждого абзаца в таблице, кроме
// последние в последней строке предотвратят разбиение таблицы на несколько страниц.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true).OfType<Cell>())
    foreach (Paragraph para in cell.Paragraphs.OfType<Paragraph>())
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### Смотрите также

* class [Row](../../row/)
* class [Cell](../)
* пространство имен [Aspose.Words.Tables](../../cell/)
* сборка [Aspose.Words](../../../)


