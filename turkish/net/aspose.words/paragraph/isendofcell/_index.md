---
title: Paragraph.IsEndOfCell
second_title: Aspose.Words for .NET API Referansı
description: Paragraph mülk. Bu paragraf bir metindeki son paragrafsa doğrudurCell  aksi halde yanlış.
type: docs
weight: 50
url: /tr/net/aspose.words/paragraph/isendofcell/
---
## Paragraph.IsEndOfCell property

Bu paragraf bir metindeki son paragrafsa doğrudur[`Cell`](../../../aspose.words.tables/cell/) ; aksi halde yanlış.

```csharp
public bool IsEndOfCell { get; }
```

### Örnekler

Aynı sayfada bir arada kalacak bir tablonun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Tablodaki her paragraf için KeepWithNext'i etkinleştirme
// son satırdaki son olanlar, tablonun birden çok sayfaya bölünmesini engeller.
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
* ad alanı [Aspose.Words](../../paragraph/)
* toplantı [Aspose.Words](../../../)


