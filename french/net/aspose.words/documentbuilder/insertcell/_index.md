---
title: DocumentBuilder.InsertCell
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Insère une cellule de tableau dans le document.
type: docs
weight: 250
url: /fr/net/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder.InsertCell method

Insère une cellule de tableau dans le document.

```csharp
public Cell InsertCell()
```

### Return_Value

Le nœud de cellule qui vient d'être inséré.

### Remarques

Pour commencer une table, il suffit d'appeler **InsérerCellule** . Après cela, tout contenu que vous ajoutez en utilisant d'autres méthodes du[`DocumentBuilder`](../) la classe sera ajoutée à la cellule actuelle.

Pour commencer une nouvelle cellule dans la même ligne, appelez **InsérerCellule** encore.

Pour terminer un appel de ligne de table[`EndRow`](../endrow/).

Utilisez le[`CellFormat`](../cellformat/)propriété pour spécifier le formatage des cellules.

### Exemples

Montre comment utiliser un générateur de document pour créer un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Démarre le tableau, puis remplit la première ligne avec deux cellules.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Appelez la méthode "EndRow" du générateur pour démarrer une nouvelle ligne.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
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

* class [Cell](../../../aspose.words.tables/cell/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


