---
title: Bookmark.IsColumn
second_title: Référence de l'API Aspose.Words pour .NET
description: Bookmark propriété. Retoursvrai si ce signet est un signet de colonne de tableau.
type: docs
weight: 40
url: /fr/net/aspose.words/bookmark/iscolumn/
---
## Bookmark.IsColumn property

Retours`vrai` si ce signet est un signet de colonne de tableau.

```csharp
public bool IsColumn { get; }
```

### Exemples

Montre comment obtenir des informations sur les signets des colonnes du tableau.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // Si un signet contient des colonnes d'un tableau, il s'agit d'un signet de colonne de tableau et son indicateur IsColumn est défini sur true.
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // Imprime le contenu de la première et de la dernière colonne entourées par le signet.
            Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
            Console.WriteLine(row.Cells[bookmark.LastColumn].GetText().TrimEnd(ControlChar.CellChar));
        }
    }
}
```

### Voir également

* class [Bookmark](../)
* espace de noms [Aspose.Words](../../bookmark/)
* Assemblée [Aspose.Words](../../../)


