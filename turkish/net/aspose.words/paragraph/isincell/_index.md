---
title: Paragraph.IsInCell
linktitle: IsInCell
articleTitle: IsInCell
second_title: Aspose.Words for .NET
description: Paragraph IsInCell mülk. Bu paragrafın doğrudan alt öğesi ise doğrudurCell  aksi halde yanlış C#'da.
type: docs
weight: 100
url: /tr/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

Bu paragrafın doğrudan alt öğesi ise doğrudur[`Cell`](../../../aspose.words.tables/cell/) ; aksi halde yanlış.

```csharp
public bool IsInCell { get; }
```

## Örnekler

Aynı sayfada bir arada kalacak bir tablonun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Tablodaki hariç her paragraf için KeepWithNext etkinleştiriliyor
// son satırdaki sonuncular tablonun birden fazla sayfaya bölünmesini engelleyecektir.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true).OfType<Cell>())
    foreach (Paragraph para in cell.Paragraphs.OfType<Paragraph>())
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### Ayrıca bakınız

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
