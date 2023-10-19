---
title: Paragraph.IsEndOfCell
linktitle: IsEndOfCell
articleTitle: IsEndOfCell
second_title: Aspose.Words for .NET
description: Paragraph IsEndOfCell mülk. Bu paragraf bir paragraftaki son paragrafsa doğrudurCell  aksi halde yanlış C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words/paragraph/isendofcell/
---
## Paragraph.IsEndOfCell property

Bu paragraf bir paragraftaki son paragrafsa doğrudur[`Cell`](../../../aspose.words.tables/cell/) ; aksi halde yanlış.

```csharp
public bool IsEndOfCell { get; }
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
