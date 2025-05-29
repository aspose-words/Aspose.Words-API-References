---
title: Table
linktitle: Table
articleTitle: Table
second_title: Aspose.Words pour .NET
description: Créez des tableaux personnalisés en toute simplicité grâce à notre constructeur de tableaux intuitif. Créez, personnalisez et optimisez l'affichage de vos données en quelques minutes !
type: docs
weight: 10
url: /fr/net/aspose.words.tables/table/table/
---
## Table constructor

Initialise une nouvelle instance du[`Table`](../) classe.

```csharp
public Table(DocumentBase doc)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| doc | DocumentBase | Le document du propriétaire. |

## Remarques

Quand[`Table`](../) est créé, il appartient au document spécifié, mais ne fait pas encore partie du document et[`ParentNode`](../../../aspose.words/node/parentnode/) est`nul`.

Pour ajouter[`Table`](../) à l'utilisation du document[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) ou[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) sur l'histoire où vous souhaitez insérer le tableau.

## Exemples

Montre comment créer un tableau.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Les tableaux contiennent des lignes, qui contiennent des cellules, qui peuvent contenir des paragraphes
// avec des éléments typiques tels que des exécutions, des formes et même d'autres tables.
// L'appel de la méthode « EnsureMinimum » sur une table garantira que
// le tableau comporte au moins une ligne, une cellule et un paragraphe.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Ajoutez du texte à la première cellule de la première ligne du tableau.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Montre comment créer un tableau imbriqué sans utiliser de générateur de documents.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Créez le tableau externe avec trois lignes et quatre colonnes, puis ajoutez-le au document.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Créez un autre tableau avec deux lignes et deux colonnes, puis insérez-le dans la première cellule du premier tableau.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Crée un nouveau tableau dans le document avec les dimensions et le texte donnés dans chaque cellule.
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    // Vous pouvez utiliser les propriétés « Titre » et « Description » pour ajouter respectivement un titre et une description à votre tableau.
    // La table doit avoir au moins une ligne avant que nous puissions utiliser ces propriétés.
    // Ces propriétés sont significatives pour les documents .docx conformes à la norme ISO / IEC 29500 (voir la classe OoxmlCompliance).
    // Si nous enregistrons le document dans des formats antérieurs à ISO/IEC 29500, Microsoft Word ignore ces propriétés.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Voir également

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
