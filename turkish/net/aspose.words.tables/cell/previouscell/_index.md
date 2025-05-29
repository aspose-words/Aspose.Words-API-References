---
title: Cell.PreviousCell
linktitle: PreviousCell
articleTitle: PreviousCell
second_title: .NET için Aspose.Words
description: Cell PreviousCell özelliği ile önceki Cell düğümüne zahmetsizce erişin. Veri gezintinizi geliştirin ve kodlama sürecinizi hızlandırın.
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

Bu yöntem, bir dosyanın hücrelerine yazılı erişime ihtiyaç duyduğunuzda kullanılabilir.[`Row`](../../row/) Eğer a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) düğüm bir hücre yerine bir satırda bulunursa, içinde bulunan bir hücreyi almak için otomatik olarak dolaştırılır

## Örnekler

Tüm tablo hücrelerinde numaralandırmanın nasıl yapılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Tablonun tüm hücrelerini numaralandır.
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
