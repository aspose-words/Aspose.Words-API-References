---
title: Bookmark.LastColumn
linktitle: LastColumn
articleTitle: LastColumn
second_title: Aspose.Words för .NET
description: Upptäck egenskapen LastColumn och få enkel åtkomst till det nollbaserade indexet för den sista kolumnen i tabellens bokmärkesområde för effektiv datahantering.
type: docs
weight: 50
url: /sv/net/aspose.words/bookmark/lastcolumn/
---
## Bookmark.LastColumn property

Hämtar det nollbaserade indexet för den sista kolumnen i tabellkolumnintervallet som är associerat med bokmärket.

```csharp
public int LastColumn { get; }
```

## Anmärkningar

Returer**-1** om detta bokmärke inte är ett bokmärke för tabellkolumner.

## Exempel

Visar hur man får information om bokmärken för tabellkolumner.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // Om ett bokmärke omsluter kolumner i en tabell är det ett bokmärke för tabellkolumner och dess IsColumn-flagga är satt till sant.
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
