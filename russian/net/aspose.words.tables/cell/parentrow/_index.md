---
title: Cell.ParentRow
second_title: Справочник по API Aspose.Words для .NET
description: Cell свойство. Возвращает родительскую строку ячейки.
type: docs
weight: 100
url: /ru/net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

Возвращает родительскую строку ячейки.

```csharp
public Row ParentRow { get; }
```

### Примечания

ЭквивалентноFirstNonMarkupParentNode брошен в[`Row`](../../row/).

### Примеры

Показывает, как настроить таблицу так, чтобы она оставалась вместе на одной странице.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Включение KeepWithNext для каждого абзаца таблицы, кроме
// последние в последней строке предотвратят разделение таблицы на несколько страниц.
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


