---
title: RowFormat.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words pour .NET
description: Découvrez la propriété RowFormat Height pour ajuster facilement la hauteur des lignes du tableau en points, améliorant ainsi la mise en page et la lisibilité de votre document.
type: docs
weight: 40
url: /fr/net/aspose.words.tables/rowformat/height/
---
## RowFormat.Height property

Obtient ou définit la hauteur de la ligne du tableau en points.

```csharp
public double Height { get; set; }
```

## Exemples

Montre comment formater des lignes avec un générateur de documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Commencez une deuxième ligne, puis configurez sa hauteur. Le générateur appliquera ces paramètres à
// sa ligne actuelle, ainsi que toutes les nouvelles lignes qu'elle crée par la suite.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// La première ligne n'a pas été affectée par la reconfiguration du remplissage et conserve toujours les valeurs par défaut.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

Montre comment créer un tableau formaté à l'aide de DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// Définissez certaines options de formatage pour l'apparence du texte et du tableau.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// La configuration des options de formatage dans un générateur de documents les appliquera
// à la cellule/ligne actuelle dans laquelle se trouve son curseur,
// ainsi que toutes les nouvelles cellules et lignes créées à l'aide de ce générateur.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Reconfigurez les objets de formatage du générateur pour les nouvelles lignes et cellules que nous sommes sur le point de créer.
// Le constructeur ne les appliquera pas à la première ligne déjà créée afin qu'elle se démarque comme une ligne d'en-tête.
builder.CellFormat.Shading.BackgroundPatternColor = Color.White;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.RowFormat.Height = 30;
builder.RowFormat.HeightRule = HeightRule.Auto;
builder.InsertCell();
builder.Font.Size = 12;
builder.Font.Bold = false;

builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");
builder.InsertCell();
builder.Write("Row 1, Cell 3.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.InsertCell();
builder.Write("Row 2, Cell 3.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateFormattedTable.docx");
```

### Voir également

* class [RowFormat](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
