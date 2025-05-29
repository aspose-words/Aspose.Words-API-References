---
title: Table.Description
linktitle: Description
articleTitle: Description
second_title: Aspose.Words pour .NET
description: Améliorez l'accessibilité de vos tableaux grâce à des propriétés descriptives. Définissez et récupérez facilement du texte alternatif pour une expérience utilisateur optimale.
type: docs
weight: 110
url: /fr/net/aspose.words.tables/table/description/
---
## Table.Description property

Obtient ou définit la description de cette table. Il fournit une représentation textuelle alternative des informations contenues dans la table.

```csharp
public string Description { get; set; }
```

## Remarques

La valeur par défaut est une chaîne vide.

Cette propriété est significative pour les documents DOCX conformes à la norme ISO/IEC 29500 ([`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/)). Lorsqu'elle est enregistrée dans des formats antérieurs à ISO/IEC 29500, la propriété est ignorée.

## Exemples

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

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
