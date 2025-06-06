---
title: AutoFitBehavior Enum
linktitle: AutoFitBehavior
articleTitle: AutoFitBehavior
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Tables.AutoFitBehavior pour optimiser le redimensionnement des tableaux avec la méthode AutoFit, améliorant ainsi la mise en page et la présentation des documents.
type: docs
weight: 7080
url: /fr/net/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enumeration

Détermine comment Aspose.Words redimensionne le tableau lorsque vous appelez le[`AutoFit`](../table/autofit/) méthode.

```csharp
public enum AutoFitBehavior
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| AutoFitToContents | `0` | Aspose.Words active l'option Ajustement automatique, supprime la largeur préférée du tableau et de toutes les cellules, puis met à jour la mise en page du tableau. |
| AutoFitToWindow | `1` | Lorsque vous utilisez cette valeur, Aspose.Words active l'option Ajustement automatique, définit la largeur préférée du tableau sur 100 %, supprime les largeurs préférées de toutes les cellules, puis met à jour la disposition du tableau. |
| FixedColumnWidths | `2` | Aspose.Words désactive l'option Ajustement automatique et supprime le favori du tableau. |

## Exemples

Montre comment créer un nouveau tableau tout en appliquant un style.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Nous devons insérer au moins une ligne avant de définir un formatage de tableau.
builder.InsertCell();

// Définissez le style de tableau utilisé en fonction de l'identifiant de style.
// Notez que tous les styles de tableau ne sont pas disponibles lors de l'enregistrement au format .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Appliquez partiellement le style aux fonctionnalités de la table en fonction des prédicats, puis créez la table.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

Montre comment créer un tableau formaté 2x2.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// Lors de la construction du tableau, le générateur de documents appliquera ses valeurs de propriété RowFormat/CellFormat actuelles
// à la ligne/cellule actuelle dans laquelle se trouve son curseur et à toutes les nouvelles lignes/cellules au fur et à mesure qu'il les crée.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Les lignes et cellules ajoutées précédemment ne sont pas affectées rétroactivement par les modifications apportées à la mise en forme du générateur.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### Voir également

* espace de noms [Aspose.Words.Tables](../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../)
