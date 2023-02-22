---
title: Paragraph.IsInCell
second_title: Aspose.Words for .NET API Referansı
description: Paragraph mülk. Bu paragraf aşağıdaki öğenin hemen alt öğesiyse doğrudurCell  aksi halde yanlış.
type: docs
weight: 100
url: /tr/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

Bu paragraf aşağıdaki öğenin hemen alt öğesiyse doğrudur[`Cell`](../../../aspose.words.tables/cell/) ; aksi halde yanlış.

```csharp
public bool IsInCell { get; }
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


