---
title: ParagraphFormat.KeepWithNext
second_title: Aspose.Words for .NET API Referansı
description: ParagraphFormat mülk. Paragraf onu takip eden paragrafla aynı sayfada kalacaksa doğrudur.
type: docs
weight: 160
url: /tr/net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

Paragraf, onu takip eden paragrafla aynı sayfada kalacaksa doğrudur.

```csharp
public bool KeepWithNext { get; set; }
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

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../paragraphformat/)
* toplantı [Aspose.Words](../../../)


