---
title: ParagraphFormat.KeepWithNext
linktitle: KeepWithNext
articleTitle: KeepWithNext
second_title: Aspose.Words for .NET
description: ParagraphFormat KeepWithNext mülk. Paragrafın onu takip eden paragrafla aynı sayfada kalması gerekiyorsa doğrudur C#'da.
type: docs
weight: 170
url: /tr/net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

Paragrafın onu takip eden paragrafla aynı sayfada kalması gerekiyorsa doğrudur.

```csharp
public bool KeepWithNext { get; set; }
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

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
