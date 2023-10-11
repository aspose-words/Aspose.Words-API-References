---
title: Row.Row
second_title: Référence de l'API Aspose.Words pour .NET
description: Row constructeur. Initialise une nouvelle instance duRow classe.
type: docs
weight: 10
url: /fr/net/aspose.words.tables/row/row/
---
## Row constructor

Initialise une nouvelle instance du[`Row`](../) classe.

```csharp
public Row(DocumentBase doc)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| doc | DocumentBase | Le document du propriétaire. |

### Remarques

Quand[`Row`](../) est créé, il appartient au document spécifié, mais ne fait pas encore partie du document et[`ParentNode`](../../../aspose.words/node/parentnode/) est`nul`.

À ajouter[`Row`](../) à l'utilisation du documentNode) ouNode) sur la table où vous souhaitez insérer la ligne.

### Exemples

Montre comment créer un tableau imbriqué sans utiliser de générateur de documents.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Créez le tableau externe avec trois lignes et quatre colonnes, puis ajoutez-le au document.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Créez un autre tableau avec deux lignes et deux colonnes puis insérez-le dans la première cellule du premier tableau.
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

    // Vous pouvez utiliser les propriétés "Titre" et "Description" pour ajouter respectivement un titre et une description à votre tableau.
    // Le tableau doit avoir au moins une ligne avant de pouvoir utiliser ces propriétés.
    // Ces propriétés sont significatives pour les documents .docx conformes à la norme ISO/IEC 29500 (voir la classe OoxmlCompliance).
    // Si nous enregistrons le document aux formats pré-ISO/IEC 29500, Microsoft Word ignore ces propriétés.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Voir également

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Row](../)
* espace de noms [Aspose.Words.Tables](../../row/)
* Assemblée [Aspose.Words](../../../)


