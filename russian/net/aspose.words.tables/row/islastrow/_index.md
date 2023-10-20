---
title: Row.IsLastRow
linktitle: IsLastRow
articleTitle: IsLastRow
second_title: Aspose.Words для .NET
description: Row IsLastRow свойство. True если это последняя строка в таблице ложь в противном случае на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

True, если это последняя строка в таблице; ложь в противном случае.

```csharp
public bool IsLastRow { get; }
```

## Примеры

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

* class [Row](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
