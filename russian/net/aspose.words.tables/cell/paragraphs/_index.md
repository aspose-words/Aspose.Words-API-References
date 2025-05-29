---
title: Cell.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Cell Paragraphs, чтобы получить доступ к коллекции прямых дочерних абзацев, улучшая структуру и читабельность документа.
type: docs
weight: 90
url: /ru/net/aspose.words.tables/cell/paragraphs/
---
## Cell.Paragraphs property

Получает коллекцию абзацев, которые являются непосредственными дочерними элементами ячейки.

```csharp
public ParagraphCollection Paragraphs { get; }
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

* class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* class [Cell](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
