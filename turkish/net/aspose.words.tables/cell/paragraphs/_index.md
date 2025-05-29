---
title: Cell.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: .NET için Aspose.Words
description: Belgenizin yapısını ve okunabilirliğini artırarak doğrudan alt paragraf koleksiyonuna erişmek için Hücre Paragrafları özelliğini keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words.tables/cell/paragraphs/
---
## Cell.Paragraphs property

Hücrenin doğrudan alt öğeleri olan paragrafların bir koleksiyonunu alır.

```csharp
public ParagraphCollection Paragraphs { get; }
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

* class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* class [Cell](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
