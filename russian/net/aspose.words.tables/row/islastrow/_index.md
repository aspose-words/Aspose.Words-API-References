---
title: Row.IsLastRow
linktitle: IsLastRow
articleTitle: IsLastRow
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Row IsLastRow. Легко определите, является ли строка последней в таблице, для упрощения управления данными и повышения эффективности программирования.
type: docs
weight: 50
url: /ru/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

True, если это последняя строка в таблице; в противном случае false.

```csharp
public bool IsLastRow { get; }
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

* class [Row](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
