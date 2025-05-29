---
title: ParagraphFormat.KeepWithNext
linktitle: KeepWithNext
articleTitle: KeepWithNext
second_title: Aspose.Words для .NET
description: Узнайте, как свойство KeepWithNext класса ParagraphFormat обеспечивает целостность абзацев, улучшая поток текста и удобочитаемость документа, придавая ему изысканный вид.
type: docs
weight: 170
url: /ru/net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

True, если абзац должен оставаться на той же странице, что и следующий за ним абзац.

```csharp
public bool KeepWithNext { get; set; }
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

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
