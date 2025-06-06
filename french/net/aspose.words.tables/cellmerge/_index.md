---
title: CellMerge Enum
linktitle: CellMerge
articleTitle: CellMerge
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Tables.CellMerge pour une fusion efficace des cellules de vos tableaux. Améliorez la mise en page de vos documents grâce à une intégration fluide et flexible.
type: docs
weight: 7120
url: /fr/net/aspose.words.tables/cellmerge/
---
## CellMerge enumeration

Spécifie comment une cellule d'un tableau est fusionnée avec d'autres cellules.

```csharp
public enum CellMerge
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | La cellule n'est pas fusionnée. |
| First | `1` | La cellule est la première cellule d'une plage de cellules fusionnées. |
| Previous | `2` | La cellule est fusionnée avec la cellule précédente horizontalement ou verticalement. |

## Exemples

Montre comment fusionner les cellules d'un tableau horizontalement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer une cellule dans la première colonne de la première ligne.
// Cette cellule sera la première d'une plage de cellules fusionnées horizontalement.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Insérer une cellule dans la deuxième colonne de la première ligne. Au lieu d'ajouter du texte,
// nous allons fusionner cette cellule avec la première cellule que nous avons ajoutée directement à gauche.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.Previous;
builder.EndRow();

// Insérer deux autres cellules non fusionnées dans la deuxième ligne.
builder.CellFormat.HorizontalMerge = CellMerge.None;
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.HorizontalMerge.docx");
```

Imprime le type de fusion horizontale et verticale d'une cellule.

```csharp
public void CheckCellsMerged()
{
    Document doc = new Document(MyDir + "Table with merged cells.docx");
    Table table = doc.FirstSection.Body.Tables[0];

    foreach (Row row in table.Rows)
        foreach (Cell cell in row.Cells)
            Console.WriteLine(PrintCellMergeType(cell));
}

public string PrintCellMergeType(Cell cell)
{
    bool isHorizontallyMerged = cell.CellFormat.HorizontalMerge != CellMerge.None;
    bool isVerticallyMerged = cell.CellFormat.VerticalMerge != CellMerge.None;
    string cellLocation =
        $"R{cell.ParentRow.ParentTable.IndexOf(cell.ParentRow) + 1}, C{cell.ParentRow.IndexOf(cell) + 1}";

    if (isHorizontallyMerged && isVerticallyMerged)
        return $"The cell at {cellLocation} is both horizontally and vertically merged";
    if (isHorizontallyMerged)
        return $"The cell at {cellLocation} is horizontally merged.";

    return isVerticallyMerged ? $"The cell at {cellLocation} is vertically merged" : $"The cell at {cellLocation} is not merged";
}
```

Montre comment fusionner les cellules d'un tableau verticalement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer une cellule dans la première colonne de la première ligne.
// Cette cellule sera la première d'une plage de cellules fusionnées verticalement.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Insérer une cellule dans la deuxième colonne de la première ligne, puis terminer la ligne.
// Configurez également le générateur pour désactiver la fusion verticale dans les cellules créées.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

 // Insérer une cellule dans la première colonne de la deuxième ligne.
// Au lieu d'ajouter du contenu textuel, nous allons fusionner cette cellule avec la première cellule que nous avons ajoutée directement au-dessus.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// Insérer une autre cellule indépendante dans la deuxième colonne de la deuxième ligne.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

### Voir également

* espace de noms [Aspose.Words.Tables](../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../)
