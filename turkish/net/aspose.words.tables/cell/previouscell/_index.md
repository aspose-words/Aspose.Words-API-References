---
title: Cell.PreviousCell
linktitle: PreviousCell
articleTitle: PreviousCell
second_title: Aspose.Words for .NET
description: Cell PreviousCell mülk. Öncekini alırCell düğüm C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.tables/cell/previouscell/
---
## Cell.PreviousCell property

Öncekini alır[`Cell`](../) düğüm.

```csharp
public Cell PreviousCell { get; }
```

## Notlar

Bu yöntem, bir hücrenin hücrelerine yazarak erişmeniz gerektiğinde kullanılabilir.[`Row`](../../row/) . Eğer a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) düğüm bir hücre yerine bir satırda bulunursa, içinde yer alan bir hücreyi elde etmek için otomatik olarak geçilir.

## Örnekler

Tüm tablo hücrelerinin nasıl numaralandırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

//Tablonun tüm hücrelerini numaralandırıyoruz.
for (Row row = table.FirstRow; row != null; row = row.NextRow)
{
    for (Cell cell = row.FirstCell; cell != null; cell = cell.NextCell)
    {
        Console.WriteLine(cell.GetText());
    }
}
```

### Ayrıca bakınız

* class [Cell](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
