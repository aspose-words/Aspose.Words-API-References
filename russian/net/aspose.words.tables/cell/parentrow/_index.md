---
title: Cell.ParentRow
linktitle: ParentRow
articleTitle: ParentRow
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Cell ParentRow, которое позволяет легко получить доступ к родительской строке любой ячейки, что повышает эффективность управления данными и навигации.
type: docs
weight: 100
url: /ru/net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

Возвращает родительскую строку ячейки.

```csharp
public Row ParentRow { get; }
```

## Примеры

Показывает, как сервировать стол так, чтобы все находились на одной странице.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Включение KeepWithNext для каждого абзаца в таблице, кроме
// последние в последней строке предотвратят разбиение таблицы на несколько страниц.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true))
    foreach (Paragraph para in cell.Paragraphs)
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
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
