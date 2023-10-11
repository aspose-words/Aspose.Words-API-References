---
title: Bookmark.FirstColumn
second_title: Aspose.Words for .NET API Referansı
description: Bookmark mülk. Yer işaretiyle ilişkili tablo sütun aralığının ilk sütununun sıfır tabanlı dizinini alır.
type: docs
weight: 30
url: /tr/net/aspose.words/bookmark/firstcolumn/
---
## Bookmark.FirstColumn property

Yer işaretiyle ilişkili tablo sütun aralığının ilk sütununun sıfır tabanlı dizinini alır.

```csharp
public int FirstColumn { get; }
```

### Notlar

İadeler **-1** bu yer imi bir tablo sütunu yer imi değilse.

### Örnekler

Tablo sütunu yer imleri hakkında nasıl bilgi alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // Bir yer işareti bir tablonun sütunlarını çevreliyorsa, bu bir tablo sütunu yer işaretidir ve IsColumn bayrağı true olarak ayarlanır.
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // Yer iminin çevrelediği ilk ve son sütunların içeriğini yazdırın.
            Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
            Console.WriteLine(row.Cells[bookmark.LastColumn].GetText().TrimEnd(ControlChar.CellChar));
        }
    }
}
```

### Ayrıca bakınız

* class [Bookmark](../)
* ad alanı [Aspose.Words](../../bookmark/)
* toplantı [Aspose.Words](../../../)


