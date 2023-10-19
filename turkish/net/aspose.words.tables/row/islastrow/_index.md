---
title: Row.IsLastRow
linktitle: IsLastRow
articleTitle: IsLastRow
second_title: Aspose.Words for .NET
description: Row IsLastRow mülk. Bu tablodaki son satırsa doğrudur aksi halde yanlış C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

Bu, tablodaki son satırsa doğrudur; aksi halde yanlış.

```csharp
public bool IsLastRow { get; }
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

* class [Row](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
