---
title: Paragraph.IsInCell
linktitle: IsInCell
articleTitle: IsInCell
second_title: Aspose.Words для .NET
description: Paragraph IsInCell свойство. True если этот абзац является непосредственным дочерним элементомCell  ложь в противном случае на С#.
type: docs
weight: 100
url: /ru/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

True, если этот абзац является непосредственным дочерним элементом[`Cell`](../../../aspose.words.tables/cell/) ; ложь в противном случае.

```csharp
public bool IsInCell { get; }
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

* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
