---
title: DocumentBuilder.EndRow
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Termine une ligne de tableau dans le document.
type: docs
weight: 220
url: /fr/net/aspose.words/documentbuilder/endrow/
---
## DocumentBuilder.EndRow method

Termine une ligne de tableau dans le document.

```csharp
public Row EndRow()
```

### Return_Value

Le nœud de ligne qui vient d'être terminé.

### Remarques

Appel **EndRow** pour terminer une ligne du tableau. Si vous appelez[`InsertCell`](../insertcell/) immédiatement après cela, le tableau continue sur une nouvelle ligne.

Utilisez le[`RowFormat`](../rowformat/) propriété pour spécifier le formatage des lignes.

### Exemples

Montre comment fusionner verticalement des cellules de tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une cellule dans la première colonne de la première ligne.
// Cette cellule sera la première d'une série de cellules fusionnées verticalement.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Insère une cellule dans la deuxième colonne de la première ligne, puis termine la ligne.
// Configurez également le générateur pour désactiver la fusion verticale dans les cellules créées.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

// Insère une cellule dans la première colonne de la deuxième ligne. 
// Au lieu d'ajouter du contenu textuel, nous fusionnerons cette cellule avec la première cellule que nous avons ajoutée directement au-dessus.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// Insère une autre cellule indépendante dans la deuxième colonne de la deuxième ligne.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

Montre comment créer un tableau 2x2 formaté.

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

// Les lignes et les cellules ajoutées précédemment ne sont pas affectées rétroactivement par les modifications apportées à la mise en forme du générateur.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

Montre comment créer un tableau avec des bordures personnalisées.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Définition des options de formatage de tableau pour un générateur de document
// les appliquera à chaque ligne et cellule que nous ajouterons avec.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// Changer la mise en forme l'appliquera à la cellule courante,
// et toutes les nouvelles cellules que nous créons avec le constructeur par la suite.
// Cela n'affectera pas les cellules que nous avons ajoutées précédemment.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Augmente la hauteur de ligne pour s'adapter au texte vertical.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Voir également

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


