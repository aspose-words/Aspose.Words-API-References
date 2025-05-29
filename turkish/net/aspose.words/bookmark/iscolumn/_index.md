---
title: Bookmark.IsColumn
linktitle: IsColumn
articleTitle: IsColumn
second_title: .NET için Aspose.Words
description: IsColumn özelliğini keşfedin. Bir yer iminin bir tablo sütununu temsil edip etmediğini kolayca belirleyerek belge gezinmenizi ve organizasyonunuzu geliştirin.
type: docs
weight: 40
url: /tr/net/aspose.words/bookmark/iscolumn/
---
## Bookmark.IsColumn property

Geri Döndürür`doğru` eğer bu yer imi bir tablo sütun yer imi ise.

```csharp
public bool IsColumn { get; }
```

## Örnekler

Tablo sütun yer imleri hakkında bilginin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // Bir yer imi bir tablonun sütunlarını kapsıyorsa, bu bir tablo sütun yer imi olur ve IsColumn bayrağı true olarak ayarlanır.
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // Yer iminin çevrelediği ilk ve son sütunların içeriğini yazdır.
            Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
            Console.WriteLine(row.Cells[bookmark.LastColumn].GetText().TrimEnd(ControlChar.CellChar));
        }
    }
}
```

### Ayrıca bakınız

* class [Bookmark](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
