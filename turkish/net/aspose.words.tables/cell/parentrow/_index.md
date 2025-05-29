---
title: Cell.ParentRow
linktitle: ParentRow
articleTitle: ParentRow
second_title: .NET için Aspose.Words
description: Herhangi bir hücrenin üst satırına kolayca erişmek için Cell ParentRow özelliğini keşfedin, böylece veri yönetiminizi ve gezinme verimliliğinizi artırın.
type: docs
weight: 100
url: /tr/net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

Hücrenin üst satırını döndürür.

```csharp
public Row ParentRow { get; }
```

## Örnekler

Aynı sayfada bir arada kalmak için bir masanın nasıl kurulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Tablodaki her paragraf için KeepWithNext'i etkinleştirme, ancak
// son satırdaki sonlar tablonun birden fazla sayfaya bölünmesini önleyecektir.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true))
    foreach (Paragraph para in cell.Paragraphs)
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### Ayrıca bakınız

* class [Row](../../row/)
* class [Cell](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
