---
title: Row.IsLastRow
second_title: Справочник по API Aspose.Words для .NET
description: Row свойство. Истинно если это последняя строка в таблице false иначе.
type: docs
weight: 50
url: /ru/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

Истинно, если это последняя строка в таблице; false иначе.

```csharp
public bool IsLastRow { get; }
```

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

* class [Row](../)
* пространство имен [Aspose.Words.Tables](../../row/)
* сборка [Aspose.Words](../../../)


