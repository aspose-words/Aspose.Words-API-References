---
title: RightPadding
second_title: Référence de l'API Aspose.Words pour .NET
description: Renvoie ou définit la quantité despace en points à ajouter à droite du contenu de la cellule.
type: docs
weight: 80
url: /fr/net/aspose.words.tables/cellformat/rightpadding/
---
## CellFormat.RightPadding property

Renvoie ou définit la quantité d'espace (en points) à ajouter à droite du contenu de la cellule.

```csharp
public double RightPadding { get; set; }
```

### Exemples

Montre comment formater des cellules avec un générateur de document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Insérez une deuxième cellule, puis configurez les options de remplissage du texte de la cellule.
// Le générateur appliquera ces paramètres à sa cellule actuelle et à toutes les nouvelles cellules créées par la suite.
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

// La première cellule n'a pas été affectée par la reconfiguration du rembourrage et contient toujours les valeurs par défaut.
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

// La première cellule grandira toujours dans le document de sortie pour correspondre à la taille de sa cellule voisine.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### Voir également

* class [CellFormat](../../cellformat)
* espace de noms [Aspose.Words.Tables](../../cellformat)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->