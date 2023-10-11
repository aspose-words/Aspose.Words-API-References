---
title: Bookmark.IsColumn
second_title: Aspose.Words för .NET API Referens
description: Bookmark fast egendom. ReturnerarSann om detta bokmärke är ett tabellkolumnbokmärke.
type: docs
weight: 40
url: /sv/net/aspose.words/bookmark/iscolumn/
---
## Bookmark.IsColumn property

Returnerar`Sann` om detta bokmärke är ett tabellkolumnbokmärke.

```csharp
public bool IsColumn { get; }
```

### Exempel

Visar hur man får information om bokmärken för tabellkolumner.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // Om ett bokmärke omsluter kolumner i en tabell, är det ett tabellkolumnbokmärke, och dess IsColumn-flagga är satt till true.
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // Skriv ut innehållet i den första och sista kolumnen som omges av bokmärket.
            Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
            Console.WriteLine(row.Cells[bookmark.LastColumn].GetText().TrimEnd(ControlChar.CellChar));
        }
    }
}
```

### Se även

* class [Bookmark](../)
* namnutrymme [Aspose.Words](../../bookmark/)
* hopsättning [Aspose.Words](../../../)


