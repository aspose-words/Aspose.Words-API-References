---
title: Row.IsLastRow
linktitle: IsLastRow
articleTitle: IsLastRow
second_title: .NET için Aspose.Words
description: Row IsLastRow özelliğini keşfedin. Kolay veri yönetimi ve gelişmiş programlama verimliliği için bir satırın tablodaki son satır olup olmadığını kolayca belirleyin.
type: docs
weight: 50
url: /tr/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

Bu tablonun son satırıysa doğru; aksi takdirde yanlış.

```csharp
public bool IsLastRow { get; }
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

* class [Row](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
