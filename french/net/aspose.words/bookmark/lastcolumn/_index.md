---
title: Bookmark.LastColumn
second_title: Référence de l'API Aspose.Words pour .NET
description: Bookmark propriété. Obtient lindex de base zéro de la dernière colonne de la plage de colonnes du tableau associée au signet.
type: docs
weight: 50
url: /fr/net/aspose.words/bookmark/lastcolumn/
---
## Bookmark.LastColumn property

Obtient l'index de base zéro de la dernière colonne de la plage de colonnes du tableau associée au signet.

```csharp
public int LastColumn { get; }
```

### Remarques

Retours **-1** si ce signet n'est pas un signet de colonne de tableau.

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


