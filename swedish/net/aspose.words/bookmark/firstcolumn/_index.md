---
title: Bookmark.FirstColumn
linktitle: FirstColumn
articleTitle: FirstColumn
second_title: Aspose.Words för .NET
description: Bookmark FirstColumn fast egendom. Hämtar det nollbaserade indexet för den första kolumnen i tabellkolumnintervallet som är associerat med bokmärket i C#.
type: docs
weight: 30
url: /sv/net/aspose.words/bookmark/firstcolumn/
---
## Bookmark.FirstColumn property

Hämtar det nollbaserade indexet för den första kolumnen i tabellkolumnintervallet som är associerat med bokmärket.

```csharp
public int FirstColumn { get; }
```

## Anmärkningar

Returnerar**-1** om detta bokmärke inte är ett tabellkolumnbokmärke.

## Exempel

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
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
