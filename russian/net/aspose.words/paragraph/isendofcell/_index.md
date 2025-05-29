---
title: Paragraph.IsEndOfCell
linktitle: IsEndOfCell
articleTitle: IsEndOfCell
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IsEndOfCell для абзацев. Узнайте, как определить, является ли абзац последним в ячейке, что улучшит структуру документа.
type: docs
weight: 50
url: /ru/net/aspose.words/paragraph/isendofcell/
---
## Paragraph.IsEndOfCell property

Истина, если этот абзац является последним абзацем в[`Cell`](../../../aspose.words.tables/cell/) ; в противном случае ложно.

```csharp
public bool IsEndOfCell { get; }
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

* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
