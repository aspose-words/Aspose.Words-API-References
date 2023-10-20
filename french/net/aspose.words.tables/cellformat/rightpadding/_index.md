---
title: CellFormat.RightPadding
linktitle: RightPadding
articleTitle: RightPadding
second_title: Aspose.Words pour .NET
description: CellFormat RightPadding propriété. Renvoie ou définit la quantité despace en points à ajouter à droite du contenu de la cellule en C#.
type: docs
weight: 80
url: /fr/net/aspose.words.tables/cellformat/rightpadding/
---
## CellFormat.RightPadding property

Renvoie ou définit la quantité d'espace (en points) à ajouter à droite du contenu de la cellule.

```csharp
public double RightPadding { get; set; }
```

## Exemples

Montre comment formater des cellules avec un générateur de documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Insère une deuxième cellule, puis configure les options de remplissage du texte des cellules.
// Le générateur appliquera ces paramètres à sa cellule actuelle, et toutes les nouvelles cellules créées par la suite.
builder.InsertCell();

CellFormat cellFormat = builder.CellFormat;
cellFormat.Width = 250;
cellFormat.LeftPadding = 30;
cellFormat.RightPadding = 30;
cellFormat.TopPadding = 30;
cellFormat.BottomPadding = 30;

builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.EndTable();

// La première cellule n'a pas été affectée par la reconfiguration du remplissage et contient toujours les valeurs par défaut.
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.Width);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.LeftPadding);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.RightPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.TopPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.BottomPadding);

Assert.AreEqual(250.0d, table.FirstRow.Cells[1].CellFormat.Width);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.LeftPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.RightPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.TopPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.BottomPadding);

// La première cellule continuera à s'agrandir dans le document de sortie pour correspondre à la taille de sa cellule voisine.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### Voir également

* class [CellFormat](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
