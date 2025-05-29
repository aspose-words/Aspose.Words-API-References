---
title: Bookmark.LastColumn
linktitle: LastColumn
articleTitle: LastColumn
second_title: .NET için Aspose.Words
description: LastColumn özelliğini keşfedin, verimli veri yönetimi için tablonuzun yer imi aralığındaki son sütunun sıfır tabanlı dizinine kolayca erişin.
type: docs
weight: 50
url: /tr/net/aspose.words/bookmark/lastcolumn/
---
## Bookmark.LastColumn property

Yer imiyle ilişkili tablo sütun aralığının son sütununun sıfır tabanlı dizinini alır.

```csharp
public int LastColumn { get; }
```

## Notlar

Geri Döndürür**-1** eğer bu yer imi bir tablo sütun yer imi değilse.

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
