---
title: Paragraph.IsInCell
linktitle: IsInCell
articleTitle: IsInCell
second_title: .NET için Aspose.Words
description: Paragraf IsInCell özelliğini keşfedin. Bir paragrafın bir Hücrenin doğrudan bir çocuğu olup olmadığını kolayca belirleyerek belge yapınızı ve biçimlendirmenizi geliştirin.
type: docs
weight: 100
url: /tr/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

Bu paragrafın doğrudan bir alt paragrafı olması durumunda doğrudur[`Cell`](../../../aspose.words.tables/cell/) ; aksi takdirde yanlış.

```csharp
public bool IsInCell { get; }
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
