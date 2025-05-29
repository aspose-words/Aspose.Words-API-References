---
title: Paragraph.IsEndOfCell
linktitle: IsEndOfCell
articleTitle: IsEndOfCell
second_title: .NET için Aspose.Words
description: Paragraflar için IsEndOfCell özelliğini keşfedin. Bir paragrafın hücredeki son paragraf olup olmadığını nasıl belirleyeceğinizi öğrenin ve belge yapınızı geliştirin.
type: docs
weight: 50
url: /tr/net/aspose.words/paragraph/isendofcell/
---
## Paragraph.IsEndOfCell property

Bu paragraf bir paragrafın son paragrafıysa doğrudur[`Cell`](../../../aspose.words.tables/cell/) ; aksi takdirde yanlış.

```csharp
public bool IsEndOfCell { get; }
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

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
